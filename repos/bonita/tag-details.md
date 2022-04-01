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
$ docker pull bonita@sha256:1aa769ecc00ae2b5c94abf43883615b7c7ecd1f9ce357edf98aeade1d04680c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:df8cf9e551041c9b64a92897b8f09852931bb461310a2bea028079ad1f76ceb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237364091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf789abfc5873ffe54f271066d876604059e84486a3bd32e099ee5be9b65ad5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:19:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:33 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:33 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:19:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:36 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:38 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:38 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:38 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1e620e691728aa8e311d14914ec09747afbb5aaeec58bb9193cba97fc5095c`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebc08e65dc3c4eeacdad4edb70beb111efdbecd2ba5e89264439a6688429d22`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b082f1b87e265e1650946efdffa368afae8fabc94d6052443a1374b67339ad`  
		Last Modified: Fri, 01 Apr 2022 18:20:38 GMT  
		Size: 116.4 MB (116415397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49cefa2fd083cf2bb942e5719e1803efaeb34805e0ce25941398e88c3b2cdd4`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5e8bfa1bea97aea8fd6ee350306915d56359c018acfaf9dcdba64cb07a57fe63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226465705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf86b4639fef9e908a16c016adca244ecf977d8379a40104883adb6ccf6ab9b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:11 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:12 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:13 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 17:40:14 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 17:40:15 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 17:40:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:40:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:40:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:40:22 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 17:40:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:40:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:40:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:40:31 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:40:33 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:40:33 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fcbe56664f56946aa07983e069a083de259a29bfa9ef3858bf4f29f2115946`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4333fdc06cc2fe3bb9e8b58460e52d8f18721e1dd9340fb2efeceb3d6574c62`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8822883e9f9b1dd8295edd1c12f56ae99da080e7c2b60482b62ba9c5ad87390`  
		Last Modified: Fri, 01 Apr 2022 17:42:34 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2eae74ce6c5c1fffd3623b25345c19d17b670976a8ef37a51e930049c58914`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:441d16032bb82790f2bf1bd068c2e14ad0cb1728534112edb792ed82e187e834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233968439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441ae7d5b88efbb9ef80dde708dacedd48f8bd7513ce74f06f5f7b83086b5988`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:17:28 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:17:31 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:17:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:17:43 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:17:45 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:17:47 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:17:49 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:17:52 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:17:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:18:02 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:18:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:18:26 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:18:31 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:18:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:02 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:21 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:23 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:25 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10028fad124e32bc756473a00b8f22e2df94b0731ef00a5962eaf2a5994b799`  
		Last Modified: Fri, 01 Apr 2022 18:23:50 GMT  
		Size: 546.8 KB (546752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bef34d8256bab1909b18380c3a7b42dd9a30fea6371ea571211879d17b46f1`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e079322111e356dd264e0548ccb1632f08ce9c3733978ec1b6a61ae8fee667d`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674c15496e13a6c3071fccd77808f458d2d3e07de9c7ff16a770915ddd896703`  
		Last Modified: Fri, 01 Apr 2022 18:24:00 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b37451ec93d4c6282ae4f1f3c0bb596a7ee8dc13e8c42744d0b5bfc819264a`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:1dc812cf6152a1dbd7dd664e0764032b903cc57c50cff56b29cd4aca4225acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:b8b90f3f8aa8a5a5a0ec94c45447c20d7e2653088cd2f92fadc0fc1adbdfe9c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15d1ac77f073ff34cd4af6e8870392ef73eb84279d0aeb4e35641c72b1ae3d4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:34:48 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:34:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 22:35:07 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 22:35:07 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 22:35:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:09 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 22:35:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 22:35:18 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 22:35:18 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 22:35:19 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 22:35:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 22:35:19 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 22:35:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918014104c9ad49400ad5b9cc91d4bcbae82a73fa5abc7a409bf899c6c43f707`  
		Last Modified: Sat, 19 Mar 2022 22:36:36 GMT  
		Size: 93.7 MB (93654889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dbdd5fbdd128de63982a3bcd426031fd93f653efb545091ac58b78a211fe`  
		Last Modified: Sat, 19 Mar 2022 22:36:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b04accad0ea54945a94640fe15c4f18217ac339546430605562903bb6e198c`  
		Last Modified: Sat, 19 Mar 2022 22:36:23 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ddf332606cb830b506954d33ba501b217b0cf296e237e53ef52a6a9a64c442`  
		Last Modified: Sat, 19 Mar 2022 22:36:22 GMT  
		Size: 1.0 MB (1003224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212fc94ac887dd5a2399140898860c0a998fe2df050fc6e32930fee44eb331d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea58fb34b6055f277ccc1d770336f1a956999418f8c74dcac36d843e5b416d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ddcab601ff797ff8b88340a09e3597f00209e58763e8cf7ed883c7c7dcb87`  
		Last Modified: Sat, 19 Mar 2022 22:36:28 GMT  
		Size: 113.7 MB (113727937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c310e4514d6b20246d217eb5e9eb415ba672947ac5986dff90d60de6cee91c`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8145813d259caf6cd0bea5d1927b07af9b65099efde705c1b7dc4b12dc186c85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282818f0e70e12d2041d5851adc6e578279aaaed15d0a8744828bf7dc42eefed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:09:07 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:09:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 15:09:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 15:09:55 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 15:09:56 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 15:09:57 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 15:09:58 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 15:09:59 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 15:10:00 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 15:10:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 15:10:02 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 15:10:03 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 15:10:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:06 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 15:10:08 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 15:10:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 15:10:29 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 15:10:29 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 15:10:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 15:10:31 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 15:10:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3433408c5fc7f4ae638ee2b5297e626eccb6ef1eaa854483eaa88fe9452b9`  
		Last Modified: Sat, 19 Mar 2022 15:12:08 GMT  
		Size: 85.8 MB (85763156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cf766653b0804c4ca85b92cc0c0069fac5a3f16d050f228364daa9898cdddc`  
		Last Modified: Sat, 19 Mar 2022 15:11:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef7cbb4cb2bf00d122900c6fc72a76a1c4ce7e507619ce147f81ef8541dd2`  
		Last Modified: Sat, 19 Mar 2022 15:11:57 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708c338db08b4e85061950c8cb417d1fdd8d11ab132c8869662712a9d49a856`  
		Last Modified: Sat, 19 Mar 2022 15:11:55 GMT  
		Size: 929.4 KB (929409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ab77260b346ebc4ffb2b67788f195a531157a6a926db586e202224550f95b5`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a15c093ce6465bc4b31ce2c94333e202d3a124194d56bb99438c8074746c3c`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0df29d03ead5b114014be21794a723b2a019942d32b8d108fe3f1f2de09ff`  
		Last Modified: Sat, 19 Mar 2022 15:12:12 GMT  
		Size: 113.7 MB (113727850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4162cb8595bb82ce1922c26bc251eadd27b261925942c84f067f35057191`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:0c8c69d7af8f945591a5d089408490bf52d5bc01ddafc64b7143d5ec6676a8ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7996e14d3d401d9e6a086fdc28917a40774b46df8ec09f0dd2d332cf566df8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:55:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:56:02 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:56:12 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:57:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:57:03 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:57:07 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 20:57:12 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:57:15 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:57:17 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:57:19 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 20:57:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 20:57:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 20:57:25 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:57:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:36 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:57:37 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 20:57:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 20:58:01 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 20:58:07 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:58:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:58:14 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:58:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54998de650aec3ff8c87077551a8a8dedbac826f959645af516a214758030de1`  
		Last Modified: Sat, 19 Mar 2022 21:00:18 GMT  
		Size: 86.6 MB (86557500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80861eb3c1c18c4914806cea4a42cc6605837eb735445fe587096738b931ba`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e3e83293caa8f19217184082aaf48f054162fd676b0bfe80c811db04b5fa07`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e62718fccbad62107b4fe7fd7a9a97a92e26d79914dbc2cd2ce19c1ae3a3e`  
		Last Modified: Sat, 19 Mar 2022 21:00:01 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ad91e85241ec6b752c76025976f23d679c8eda783616cb3d8830044dcb21a`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaebf6593ed9f193fbd8172caa14b34ddf91ceab1a3dc48c01ad9e695794966`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d1d821c92f5f66422e0625adaed7d15289260431916f065c873a51902db85`  
		Last Modified: Sat, 19 Mar 2022 21:00:10 GMT  
		Size: 113.7 MB (113727951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730acde910ffb0b1920533e60561ebf0826b19c5d57baa84709e782722f8539`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:1dc812cf6152a1dbd7dd664e0764032b903cc57c50cff56b29cd4aca4225acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:b8b90f3f8aa8a5a5a0ec94c45447c20d7e2653088cd2f92fadc0fc1adbdfe9c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15d1ac77f073ff34cd4af6e8870392ef73eb84279d0aeb4e35641c72b1ae3d4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:34:48 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:34:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 22:35:07 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 22:35:07 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 22:35:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:09 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 22:35:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 22:35:18 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 22:35:18 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 22:35:19 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 22:35:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 22:35:19 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 22:35:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918014104c9ad49400ad5b9cc91d4bcbae82a73fa5abc7a409bf899c6c43f707`  
		Last Modified: Sat, 19 Mar 2022 22:36:36 GMT  
		Size: 93.7 MB (93654889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dbdd5fbdd128de63982a3bcd426031fd93f653efb545091ac58b78a211fe`  
		Last Modified: Sat, 19 Mar 2022 22:36:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b04accad0ea54945a94640fe15c4f18217ac339546430605562903bb6e198c`  
		Last Modified: Sat, 19 Mar 2022 22:36:23 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ddf332606cb830b506954d33ba501b217b0cf296e237e53ef52a6a9a64c442`  
		Last Modified: Sat, 19 Mar 2022 22:36:22 GMT  
		Size: 1.0 MB (1003224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212fc94ac887dd5a2399140898860c0a998fe2df050fc6e32930fee44eb331d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea58fb34b6055f277ccc1d770336f1a956999418f8c74dcac36d843e5b416d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ddcab601ff797ff8b88340a09e3597f00209e58763e8cf7ed883c7c7dcb87`  
		Last Modified: Sat, 19 Mar 2022 22:36:28 GMT  
		Size: 113.7 MB (113727937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c310e4514d6b20246d217eb5e9eb415ba672947ac5986dff90d60de6cee91c`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8145813d259caf6cd0bea5d1927b07af9b65099efde705c1b7dc4b12dc186c85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282818f0e70e12d2041d5851adc6e578279aaaed15d0a8744828bf7dc42eefed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:09:07 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:09:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 15:09:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 15:09:55 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 15:09:56 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 15:09:57 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 15:09:58 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 15:09:59 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 15:10:00 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 15:10:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 15:10:02 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 15:10:03 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 15:10:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:06 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 15:10:08 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 15:10:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 15:10:29 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 15:10:29 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 15:10:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 15:10:31 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 15:10:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3433408c5fc7f4ae638ee2b5297e626eccb6ef1eaa854483eaa88fe9452b9`  
		Last Modified: Sat, 19 Mar 2022 15:12:08 GMT  
		Size: 85.8 MB (85763156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cf766653b0804c4ca85b92cc0c0069fac5a3f16d050f228364daa9898cdddc`  
		Last Modified: Sat, 19 Mar 2022 15:11:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef7cbb4cb2bf00d122900c6fc72a76a1c4ce7e507619ce147f81ef8541dd2`  
		Last Modified: Sat, 19 Mar 2022 15:11:57 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708c338db08b4e85061950c8cb417d1fdd8d11ab132c8869662712a9d49a856`  
		Last Modified: Sat, 19 Mar 2022 15:11:55 GMT  
		Size: 929.4 KB (929409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ab77260b346ebc4ffb2b67788f195a531157a6a926db586e202224550f95b5`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a15c093ce6465bc4b31ce2c94333e202d3a124194d56bb99438c8074746c3c`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0df29d03ead5b114014be21794a723b2a019942d32b8d108fe3f1f2de09ff`  
		Last Modified: Sat, 19 Mar 2022 15:12:12 GMT  
		Size: 113.7 MB (113727850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4162cb8595bb82ce1922c26bc251eadd27b261925942c84f067f35057191`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:0c8c69d7af8f945591a5d089408490bf52d5bc01ddafc64b7143d5ec6676a8ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7996e14d3d401d9e6a086fdc28917a40774b46df8ec09f0dd2d332cf566df8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:55:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:56:02 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:56:12 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:57:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:57:03 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:57:07 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 20:57:12 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:57:15 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:57:17 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:57:19 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 20:57:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 20:57:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 20:57:25 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:57:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:36 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:57:37 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 20:57:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 20:58:01 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 20:58:07 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:58:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:58:14 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:58:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54998de650aec3ff8c87077551a8a8dedbac826f959645af516a214758030de1`  
		Last Modified: Sat, 19 Mar 2022 21:00:18 GMT  
		Size: 86.6 MB (86557500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80861eb3c1c18c4914806cea4a42cc6605837eb735445fe587096738b931ba`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e3e83293caa8f19217184082aaf48f054162fd676b0bfe80c811db04b5fa07`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e62718fccbad62107b4fe7fd7a9a97a92e26d79914dbc2cd2ce19c1ae3a3e`  
		Last Modified: Sat, 19 Mar 2022 21:00:01 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ad91e85241ec6b752c76025976f23d679c8eda783616cb3d8830044dcb21a`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaebf6593ed9f193fbd8172caa14b34ddf91ceab1a3dc48c01ad9e695794966`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d1d821c92f5f66422e0625adaed7d15289260431916f065c873a51902db85`  
		Last Modified: Sat, 19 Mar 2022 21:00:10 GMT  
		Size: 113.7 MB (113727951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730acde910ffb0b1920533e60561ebf0826b19c5d57baa84709e782722f8539`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1`

```console
$ docker pull bonita@sha256:dbe41ab9ee8c3caa42cc5e1125ee8a2572faf02a4bc1c5cbedb3dbc0ddb82990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1` - linux; amd64

```console
$ docker pull bonita@sha256:72ba4fd5c5b5e75b4a4aac891e95a4a708b3fcff5448a82d44433a3e178baf60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3122e6b976281e453833fbfda09b1455e6dc94e24cdef01ca341319ace1d23c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:19:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:19:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:19:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:19:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:50 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:19:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:19:58 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:19:59 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:19:59 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:19:59 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:19:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:19:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e79f563d8aab8c0eba270cec8a016d662c148be1c254ec76d50ad5486cc1b4`  
		Last Modified: Fri, 01 Apr 2022 18:21:02 GMT  
		Size: 60.7 MB (60744597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa255d535aa1bf014e65f4e1d6b0fa40cba553688081c9a78c29b690676b93`  
		Last Modified: Fri, 01 Apr 2022 18:20:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669df2ea372e0ec60d6bea4820d349f0a3748a25ebc6819b4f93d4bcc4c8a398`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d10b61b855ba40ce63a4ca04403f7ee25ed4d8d79592e04779032096d64866`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef831ba0489b62722b56ccc4d5a24ad3e2a6928c455499930f91088a07f852dd`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9264ea8039ded28c2527884eda40ad24b08e27b1d3c9f459b889ea332fb55b92`  
		Last Modified: Fri, 01 Apr 2022 18:20:58 GMT  
		Size: 116.7 MB (116690816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9672a4c884851bccaeebbb6edcec8b9e4ef7588b0568aec71d0eac982b510851`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:50c970cdd14d323dd1c99745ae3925ba8208a92c9042696bae707a54b14517e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0918abc89121ebb476786f81746682254ced77a57c4cfc7739ce22ff513a8de`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 17:40:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 17:40:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 17:40:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 17:40:51 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:52 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:53 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:54 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:55 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:56 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 17:40:57 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 17:40:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 17:40:59 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:41:01 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:02 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:41:04 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 17:41:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 17:41:12 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 17:41:13 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 17:41:14 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 17:41:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 17:41:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 17:41:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 17:41:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 17:41:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 17:41:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 17:41:21 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 17:41:22 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 17:41:23 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 17:41:24 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 17:41:26 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 17:41:26 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 17:41:27 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 17:41:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4f822664704f6f79949aefca413d12eb17df87a9aadd95325020d1a6a9b9b`  
		Last Modified: Fri, 01 Apr 2022 17:43:02 GMT  
		Size: 60.1 MB (60067359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c616b6eca14fdd3df9fc774463c6ab0e906bfe7cdce04ce4da0818a5efd5a6`  
		Last Modified: Fri, 01 Apr 2022 17:42:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2d80d2d31fe74211a2e1feb10facc69bccfb5545f85f445b8bd901fed497f`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ce5132c23db90ca4ba8609f07532a889517754b7497ce4cf02a58a49c6b11`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5f63b232f4b68842b3891c68aeae172a15809c56a149747b5e88a78ba793cc`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 3.0 KB (2998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1c56ddddc60c65d81eea0ab6a218f73a0a2bbd1f1a2dc46dafa1a20df5e696`  
		Last Modified: Fri, 01 Apr 2022 17:43:04 GMT  
		Size: 116.7 MB (116688763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a3aab75707fb0e9f2cae8205a791a83ccfdfa51d46f778107d78fd2531e59d`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:4eafff51214222baf590717b558ab80c9e3b3dc89ecf9fb95af96e0b4277ecf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176074668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e45f2da93ca22ec79676dbdf673af55a554f680e979a353255374346ddadb8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:16:52 GMT
ADD file:9e7b65a431d59070abaadae56d9c3fc59c899af881939e4353b1f524b2bd5185 in / 
# Tue, 29 Mar 2022 00:16:55 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:20:17 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:20:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:20:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:20:43 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:20:46 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:20:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:20:50 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:20:52 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:20:54 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:20:56 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:20:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:21:01 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:21:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:19 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:21:20 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:21:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:21:50 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:21:57 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:22:02 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:22:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:22:10 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:22:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:22:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:22:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:22:21 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:22:25 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:22:33 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:22:39 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:22:45 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:22:48 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:22:50 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:22:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:23:04 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1c611bca4fa49cac5bc1e3826ad53fee85ed659d24bffcccd86c3f04be07339a`  
		Last Modified: Tue, 29 Mar 2022 00:18:26 GMT  
		Size: 2.8 MB (2811009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c49f5b4939e43318833abc91f2f281812dd7be534bc1abc9b5c00bdff8592d0`  
		Last Modified: Fri, 01 Apr 2022 18:24:33 GMT  
		Size: 56.6 MB (56562818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68fd31f2119b8e80ee813acd91a33add2bb6ca795a12816046c44571cca10ff`  
		Last Modified: Fri, 01 Apr 2022 18:24:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac3c3ae00e0450c3436310816fa5a5c2a5a0d7d6a7f6db788bf73d2f22a02f9`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3a61437e3af23539f3a2e0826774e6e4055fd807f5c1f7468d6121b852fc04`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70757e12053925c257cca583ad4bd53f04208ab8b8726a85dcf5152bba7542c1`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 3.0 KB (3038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cf4564c5e52458dca4281258184644faa08ab0e5097bbe95ba7c8feab3aba4`  
		Last Modified: Fri, 01 Apr 2022 18:24:30 GMT  
		Size: 116.7 MB (116690818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17eda15dd05eb4b902ea75e5e95dec04a448b4c1ebe78d3c29374b9e7a93486`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2022.1-u0`

```console
$ docker pull bonita@sha256:dbe41ab9ee8c3caa42cc5e1125ee8a2572faf02a4bc1c5cbedb3dbc0ddb82990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2022.1-u0` - linux; amd64

```console
$ docker pull bonita@sha256:72ba4fd5c5b5e75b4a4aac891e95a4a708b3fcff5448a82d44433a3e178baf60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3122e6b976281e453833fbfda09b1455e6dc94e24cdef01ca341319ace1d23c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:19:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:19:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:19:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:19:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:50 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:19:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:19:58 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:19:59 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:19:59 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:19:59 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:19:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:19:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e79f563d8aab8c0eba270cec8a016d662c148be1c254ec76d50ad5486cc1b4`  
		Last Modified: Fri, 01 Apr 2022 18:21:02 GMT  
		Size: 60.7 MB (60744597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa255d535aa1bf014e65f4e1d6b0fa40cba553688081c9a78c29b690676b93`  
		Last Modified: Fri, 01 Apr 2022 18:20:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669df2ea372e0ec60d6bea4820d349f0a3748a25ebc6819b4f93d4bcc4c8a398`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d10b61b855ba40ce63a4ca04403f7ee25ed4d8d79592e04779032096d64866`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef831ba0489b62722b56ccc4d5a24ad3e2a6928c455499930f91088a07f852dd`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9264ea8039ded28c2527884eda40ad24b08e27b1d3c9f459b889ea332fb55b92`  
		Last Modified: Fri, 01 Apr 2022 18:20:58 GMT  
		Size: 116.7 MB (116690816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9672a4c884851bccaeebbb6edcec8b9e4ef7588b0568aec71d0eac982b510851`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:50c970cdd14d323dd1c99745ae3925ba8208a92c9042696bae707a54b14517e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0918abc89121ebb476786f81746682254ced77a57c4cfc7739ce22ff513a8de`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 17:40:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 17:40:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 17:40:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 17:40:51 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:52 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:53 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:54 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:55 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:56 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 17:40:57 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 17:40:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 17:40:59 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:41:01 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:02 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:41:04 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 17:41:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 17:41:12 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 17:41:13 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 17:41:14 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 17:41:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 17:41:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 17:41:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 17:41:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 17:41:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 17:41:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 17:41:21 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 17:41:22 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 17:41:23 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 17:41:24 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 17:41:26 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 17:41:26 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 17:41:27 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 17:41:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4f822664704f6f79949aefca413d12eb17df87a9aadd95325020d1a6a9b9b`  
		Last Modified: Fri, 01 Apr 2022 17:43:02 GMT  
		Size: 60.1 MB (60067359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c616b6eca14fdd3df9fc774463c6ab0e906bfe7cdce04ce4da0818a5efd5a6`  
		Last Modified: Fri, 01 Apr 2022 17:42:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2d80d2d31fe74211a2e1feb10facc69bccfb5545f85f445b8bd901fed497f`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ce5132c23db90ca4ba8609f07532a889517754b7497ce4cf02a58a49c6b11`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5f63b232f4b68842b3891c68aeae172a15809c56a149747b5e88a78ba793cc`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 3.0 KB (2998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1c56ddddc60c65d81eea0ab6a218f73a0a2bbd1f1a2dc46dafa1a20df5e696`  
		Last Modified: Fri, 01 Apr 2022 17:43:04 GMT  
		Size: 116.7 MB (116688763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a3aab75707fb0e9f2cae8205a791a83ccfdfa51d46f778107d78fd2531e59d`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2022.1-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:4eafff51214222baf590717b558ab80c9e3b3dc89ecf9fb95af96e0b4277ecf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176074668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e45f2da93ca22ec79676dbdf673af55a554f680e979a353255374346ddadb8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:16:52 GMT
ADD file:9e7b65a431d59070abaadae56d9c3fc59c899af881939e4353b1f524b2bd5185 in / 
# Tue, 29 Mar 2022 00:16:55 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:20:17 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:20:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:20:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:20:43 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:20:46 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:20:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:20:50 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:20:52 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:20:54 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:20:56 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:20:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:21:01 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:21:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:19 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:21:20 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:21:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:21:50 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:21:57 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:22:02 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:22:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:22:10 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:22:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:22:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:22:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:22:21 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:22:25 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:22:33 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:22:39 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:22:45 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:22:48 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:22:50 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:22:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:23:04 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1c611bca4fa49cac5bc1e3826ad53fee85ed659d24bffcccd86c3f04be07339a`  
		Last Modified: Tue, 29 Mar 2022 00:18:26 GMT  
		Size: 2.8 MB (2811009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c49f5b4939e43318833abc91f2f281812dd7be534bc1abc9b5c00bdff8592d0`  
		Last Modified: Fri, 01 Apr 2022 18:24:33 GMT  
		Size: 56.6 MB (56562818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68fd31f2119b8e80ee813acd91a33add2bb6ca795a12816046c44571cca10ff`  
		Last Modified: Fri, 01 Apr 2022 18:24:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac3c3ae00e0450c3436310816fa5a5c2a5a0d7d6a7f6db788bf73d2f22a02f9`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3a61437e3af23539f3a2e0826774e6e4055fd807f5c1f7468d6121b852fc04`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70757e12053925c257cca583ad4bd53f04208ab8b8726a85dcf5152bba7542c1`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 3.0 KB (3038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cf4564c5e52458dca4281258184644faa08ab0e5097bbe95ba7c8feab3aba4`  
		Last Modified: Fri, 01 Apr 2022 18:24:30 GMT  
		Size: 116.7 MB (116690818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17eda15dd05eb4b902ea75e5e95dec04a448b4c1ebe78d3c29374b9e7a93486`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:caa92875a4e4abdc3151ed03620cd7d5e7d062feb148f66585d6074b6cfd531c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:925fbecf5f86d5cae2c3bf402f137c5850dc48d597c4bd1492fca24eb9da4569
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234296474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac5ff240553f524b9bc9c2257bda4b04b677232a1f7918222e274d049cd247`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 01 Apr 2022 18:19:18 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 18:19:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:20 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 01 Apr 2022 18:19:25 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:27 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:27 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:27 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:27 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec89a5d27c97fd5697654d619e71f11dca487abeed4da399ba484618d8562fb`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31cc31dc0e2edb0d37bc6020745d095ba7ef1738644a2add7b3aff50f0510ba`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ed41f555e5d8e3c5df3e4160decc88729049fa669074f8a6a7e1df1542cf2d`  
		Last Modified: Fri, 01 Apr 2022 18:20:22 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1648688f44a0e2fb120535ef6ee1c01f5c3a0a0fd3d332c9038fcb020e6ef43b`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5b761d9ea81e5200e3675f41f85a95f4298c9caef23e0ea6fbe001d3111b9811
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223398072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f778aeb74eaa7e50743d5efbf03cd3c55224a737a534f12146d3cb1b18d914`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:39:38 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:39:39 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:39:40 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:39:41 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 01 Apr 2022 17:39:42 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 01 Apr 2022 17:39:43 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 17:39:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:39:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 17:39:46 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:39:47 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:39:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 01 Apr 2022 17:39:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:39:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:39:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:39:57 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:39:59 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:39:59 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:00 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4751730c21c09d59f824c9c01dc4cce16a8d741be9072c50f5adc8bd08e7d0`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b6fd8b941c9f1003031fd2444c87dd52b8470aa6b6ffebdea19c32590f13e3`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 6.9 KB (6865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bbd297c66d682be8375738a7ff3b97bb7f535a884ff4dd5d479027ea7dd650`  
		Last Modified: Fri, 01 Apr 2022 17:42:13 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92efa6a889c84d53b52cfbf3f19443fe64f95d8ed08127fca1ed6927ad809eea`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:d16ea974e04bd4f761f67994ccc5d5624979db582d507c2958d3f870fbab3f88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230900848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9ef5c8715617b7a80a200ac195558cb116f45f37925d8739f3603215b5021e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:50:29 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:50:32 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:50:35 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:50:40 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:50:43 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:50:45 GMT
ENV BONITA_VERSION=7.11.4
# Sat, 19 Mar 2022 20:50:51 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Sat, 19 Mar 2022 20:51:03 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Sat, 19 Mar 2022 20:51:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:51:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Sat, 19 Mar 2022 20:51:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 19 Mar 2022 20:51:39 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:51:40 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Sat, 19 Mar 2022 20:51:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Sat, 19 Mar 2022 20:51:58 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 19 Mar 2022 20:52:03 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 19 Mar 2022 20:52:05 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:52:07 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:52:09 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:52:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0bed89b849d63e13572d4bd1f077ac7051d8690ed5f7b2a7ee9f31235c407a`  
		Last Modified: Sat, 19 Mar 2022 20:59:05 GMT  
		Size: 546.8 KB (546771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebc57ec54343963dbbc5c48b04500239581d1365e6db96cefe43e2e8ed21e8e`  
		Last Modified: Sat, 19 Mar 2022 20:59:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af31894a70c1b8382c27ee2315c3dd303a7f07fd2d75cc4460cf168169eff9a`  
		Last Modified: Sat, 19 Mar 2022 20:59:05 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9689812f93fa2920862b8e121c3ce42e84f83176e16bc32c4a1d8b820eae6a3e`  
		Last Modified: Sat, 19 Mar 2022 20:59:13 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bee7cf5f74b0357e0a79f4f64270f610ef989226329b53084744dc5da4ae8a`  
		Last Modified: Sat, 19 Mar 2022 20:59:05 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:caa92875a4e4abdc3151ed03620cd7d5e7d062feb148f66585d6074b6cfd531c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:925fbecf5f86d5cae2c3bf402f137c5850dc48d597c4bd1492fca24eb9da4569
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234296474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecac5ff240553f524b9bc9c2257bda4b04b677232a1f7918222e274d049cd247`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 01 Apr 2022 18:19:18 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 18:19:18 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:19 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 18:19:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:20 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 01 Apr 2022 18:19:25 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:27 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:27 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:27 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:27 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:28 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec89a5d27c97fd5697654d619e71f11dca487abeed4da399ba484618d8562fb`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f31cc31dc0e2edb0d37bc6020745d095ba7ef1738644a2add7b3aff50f0510ba`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ed41f555e5d8e3c5df3e4160decc88729049fa669074f8a6a7e1df1542cf2d`  
		Last Modified: Fri, 01 Apr 2022 18:20:22 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1648688f44a0e2fb120535ef6ee1c01f5c3a0a0fd3d332c9038fcb020e6ef43b`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5b761d9ea81e5200e3675f41f85a95f4298c9caef23e0ea6fbe001d3111b9811
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223398072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07f778aeb74eaa7e50743d5efbf03cd3c55224a737a534f12146d3cb1b18d914`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:39:38 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:39:39 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:39:40 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:39:41 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 01 Apr 2022 17:39:42 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 01 Apr 2022 17:39:43 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 17:39:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:39:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 01 Apr 2022 17:39:46 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:39:47 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:39:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 01 Apr 2022 17:39:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:39:55 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:39:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:39:57 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:39:59 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:39:59 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:00 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c4751730c21c09d59f824c9c01dc4cce16a8d741be9072c50f5adc8bd08e7d0`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b6fd8b941c9f1003031fd2444c87dd52b8470aa6b6ffebdea19c32590f13e3`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 6.9 KB (6865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bbd297c66d682be8375738a7ff3b97bb7f535a884ff4dd5d479027ea7dd650`  
		Last Modified: Fri, 01 Apr 2022 17:42:13 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92efa6a889c84d53b52cfbf3f19443fe64f95d8ed08127fca1ed6927ad809eea`  
		Last Modified: Fri, 01 Apr 2022 17:42:04 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:d16ea974e04bd4f761f67994ccc5d5624979db582d507c2958d3f870fbab3f88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230900848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9ef5c8715617b7a80a200ac195558cb116f45f37925d8739f3603215b5021e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:50:29 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:50:32 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:50:35 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:50:40 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:50:43 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:50:45 GMT
ENV BONITA_VERSION=7.11.4
# Sat, 19 Mar 2022 20:50:51 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Sat, 19 Mar 2022 20:51:03 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Sat, 19 Mar 2022 20:51:15 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:51:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Sat, 19 Mar 2022 20:51:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Sat, 19 Mar 2022 20:51:39 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:51:40 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Sat, 19 Mar 2022 20:51:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Sat, 19 Mar 2022 20:51:58 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Sat, 19 Mar 2022 20:52:03 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Sat, 19 Mar 2022 20:52:05 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:52:07 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:52:09 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:52:12 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0bed89b849d63e13572d4bd1f077ac7051d8690ed5f7b2a7ee9f31235c407a`  
		Last Modified: Sat, 19 Mar 2022 20:59:05 GMT  
		Size: 546.8 KB (546771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebc57ec54343963dbbc5c48b04500239581d1365e6db96cefe43e2e8ed21e8e`  
		Last Modified: Sat, 19 Mar 2022 20:59:05 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7af31894a70c1b8382c27ee2315c3dd303a7f07fd2d75cc4460cf168169eff9a`  
		Last Modified: Sat, 19 Mar 2022 20:59:05 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9689812f93fa2920862b8e121c3ce42e84f83176e16bc32c4a1d8b820eae6a3e`  
		Last Modified: Sat, 19 Mar 2022 20:59:13 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0bee7cf5f74b0357e0a79f4f64270f610ef989226329b53084744dc5da4ae8a`  
		Last Modified: Sat, 19 Mar 2022 20:59:05 GMT  
		Size: 1.7 KB (1713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:1aa769ecc00ae2b5c94abf43883615b7c7ecd1f9ce357edf98aeade1d04680c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:df8cf9e551041c9b64a92897b8f09852931bb461310a2bea028079ad1f76ceb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237364091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf789abfc5873ffe54f271066d876604059e84486a3bd32e099ee5be9b65ad5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:19:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:33 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:33 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:19:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:36 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:38 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:38 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:38 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1e620e691728aa8e311d14914ec09747afbb5aaeec58bb9193cba97fc5095c`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebc08e65dc3c4eeacdad4edb70beb111efdbecd2ba5e89264439a6688429d22`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b082f1b87e265e1650946efdffa368afae8fabc94d6052443a1374b67339ad`  
		Last Modified: Fri, 01 Apr 2022 18:20:38 GMT  
		Size: 116.4 MB (116415397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49cefa2fd083cf2bb942e5719e1803efaeb34805e0ce25941398e88c3b2cdd4`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5e8bfa1bea97aea8fd6ee350306915d56359c018acfaf9dcdba64cb07a57fe63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226465705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf86b4639fef9e908a16c016adca244ecf977d8379a40104883adb6ccf6ab9b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:11 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:12 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:13 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 17:40:14 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 17:40:15 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 17:40:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:40:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:40:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:40:22 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 17:40:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:40:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:40:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:40:31 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:40:33 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:40:33 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fcbe56664f56946aa07983e069a083de259a29bfa9ef3858bf4f29f2115946`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4333fdc06cc2fe3bb9e8b58460e52d8f18721e1dd9340fb2efeceb3d6574c62`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8822883e9f9b1dd8295edd1c12f56ae99da080e7c2b60482b62ba9c5ad87390`  
		Last Modified: Fri, 01 Apr 2022 17:42:34 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2eae74ce6c5c1fffd3623b25345c19d17b670976a8ef37a51e930049c58914`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:441d16032bb82790f2bf1bd068c2e14ad0cb1728534112edb792ed82e187e834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233968439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441ae7d5b88efbb9ef80dde708dacedd48f8bd7513ce74f06f5f7b83086b5988`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:17:28 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:17:31 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:17:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:17:43 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:17:45 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:17:47 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:17:49 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:17:52 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:17:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:18:02 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:18:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:18:26 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:18:31 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:18:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:02 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:21 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:23 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:25 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10028fad124e32bc756473a00b8f22e2df94b0731ef00a5962eaf2a5994b799`  
		Last Modified: Fri, 01 Apr 2022 18:23:50 GMT  
		Size: 546.8 KB (546752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bef34d8256bab1909b18380c3a7b42dd9a30fea6371ea571211879d17b46f1`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e079322111e356dd264e0548ccb1632f08ce9c3733978ec1b6a61ae8fee667d`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674c15496e13a6c3071fccd77808f458d2d3e07de9c7ff16a770915ddd896703`  
		Last Modified: Fri, 01 Apr 2022 18:24:00 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b37451ec93d4c6282ae4f1f3c0bb596a7ee8dc13e8c42744d0b5bfc819264a`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:1aa769ecc00ae2b5c94abf43883615b7c7ecd1f9ce357edf98aeade1d04680c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:df8cf9e551041c9b64a92897b8f09852931bb461310a2bea028079ad1f76ceb3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.4 MB (237364091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbf789abfc5873ffe54f271066d876604059e84486a3bd32e099ee5be9b65ad5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:33:12 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:33:13 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:19:18 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:19:18 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:19:31 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:19:32 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:32 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:19:32 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:19:33 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:33 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:19:35 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:36 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:38 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:38 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:38 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:38 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b243b914b9e4b6fb7ac97f6985856105df397ebe953a46a891d3fb61e19cd188`  
		Last Modified: Sat, 19 Mar 2022 22:35:54 GMT  
		Size: 93.7 MB (93652268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13c137b851e3462a6945dd8eba41e1c5d25719ead032e2a0b5f2ec5246218e6d`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81f6bd5a2ca725536cdf2adb96200b6c1e2e06302b461f5697abbcde1daefa5b`  
		Last Modified: Sat, 19 Mar 2022 22:35:41 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5408a5c3d28f5db2f4a93cc60518c04d21f4af13f6e006bf62a7fc24f85173`  
		Last Modified: Fri, 01 Apr 2022 18:20:17 GMT  
		Size: 577.0 KB (576954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1e620e691728aa8e311d14914ec09747afbb5aaeec58bb9193cba97fc5095c`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ebc08e65dc3c4eeacdad4edb70beb111efdbecd2ba5e89264439a6688429d22`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 6.9 KB (6943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b082f1b87e265e1650946efdffa368afae8fabc94d6052443a1374b67339ad`  
		Last Modified: Fri, 01 Apr 2022 18:20:38 GMT  
		Size: 116.4 MB (116415397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49cefa2fd083cf2bb942e5719e1803efaeb34805e0ce25941398e88c3b2cdd4`  
		Last Modified: Fri, 01 Apr 2022 18:20:33 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5e8bfa1bea97aea8fd6ee350306915d56359c018acfaf9dcdba64cb07a57fe63
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226465705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf86b4639fef9e908a16c016adca244ecf977d8379a40104883adb6ccf6ab9b`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:06:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:06:55 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:06:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 17:39:37 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 17:39:37 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:10 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:11 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:12 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:13 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 17:40:14 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 17:40:15 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 17:40:16 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:17 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:40:18 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 17:40:19 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 17:40:20 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:40:22 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 17:40:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 17:40:29 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 17:40:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 17:40:31 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 17:40:33 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 17:40:33 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 17:40:34 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a6aca795d67851a5bf64ff69de8a2c846040a785e02ab939c669ea1259dead`  
		Last Modified: Sat, 19 Mar 2022 15:11:16 GMT  
		Size: 85.8 MB (85763563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bdcf2d35ac4a0024417899c05e98131a4fff9dc84f1e8c8adc753bdce04155`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccf8ec78bd0d33bfd948482e9fddfc7b40d51477334e11b6fb2e7ef30e6edb77`  
		Last Modified: Sat, 19 Mar 2022 15:11:05 GMT  
		Size: 1.9 KB (1862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88401d98730bd08397935fa1a16cdf899eb6a7ca95ad6c285bcbcdc2dbe71032`  
		Last Modified: Fri, 01 Apr 2022 17:42:05 GMT  
		Size: 546.9 KB (546930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94fcbe56664f56946aa07983e069a083de259a29bfa9ef3858bf4f29f2115946`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4333fdc06cc2fe3bb9e8b58460e52d8f18721e1dd9340fb2efeceb3d6574c62`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 6.9 KB (6919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8822883e9f9b1dd8295edd1c12f56ae99da080e7c2b60482b62ba9c5ad87390`  
		Last Modified: Fri, 01 Apr 2022 17:42:34 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2eae74ce6c5c1fffd3623b25345c19d17b670976a8ef37a51e930049c58914`  
		Last Modified: Fri, 01 Apr 2022 17:42:24 GMT  
		Size: 1.7 KB (1684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:441d16032bb82790f2bf1bd068c2e14ad0cb1728534112edb792ed82e187e834
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233968439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:441ae7d5b88efbb9ef80dde708dacedd48f8bd7513ce74f06f5f7b83086b5988`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:49:46 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:49:56 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Apr 2022 18:17:28 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Apr 2022 18:17:31 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:17:36 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:17:43 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:17:45 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:17:47 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:17:49 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Apr 2022 18:17:52 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Apr 2022 18:17:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Apr 2022 18:18:02 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:18:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Apr 2022 18:18:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Apr 2022 18:18:26 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:18:31 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Apr 2022 18:18:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Apr 2022 18:19:02 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Apr 2022 18:19:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Apr 2022 18:19:21 GMT
VOLUME [/opt/bonita]
# Fri, 01 Apr 2022 18:19:23 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Apr 2022 18:19:25 GMT
EXPOSE 8080
# Fri, 01 Apr 2022 18:19:29 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29745dd35ee1f69790cb70dafe2654f253a2638e23c28c77381c2a35be5ae34`  
		Last Modified: Sat, 19 Mar 2022 20:59:23 GMT  
		Size: 86.6 MB (86557393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f81968045c994cb7690d1dc9d02c0dafbd65aa7250aa87e3ecb5a33d1f6873a`  
		Last Modified: Sat, 19 Mar 2022 20:59:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e298445fac0e7aca27b8ba8df16b18493ea21a96401f4545613ffd08bcc7c7a1`  
		Last Modified: Sat, 19 Mar 2022 20:59:08 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10028fad124e32bc756473a00b8f22e2df94b0731ef00a5962eaf2a5994b799`  
		Last Modified: Fri, 01 Apr 2022 18:23:50 GMT  
		Size: 546.8 KB (546752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bef34d8256bab1909b18380c3a7b42dd9a30fea6371ea571211879d17b46f1`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e079322111e356dd264e0548ccb1632f08ce9c3733978ec1b6a61ae8fee667d`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 6.9 KB (6940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674c15496e13a6c3071fccd77808f458d2d3e07de9c7ff16a770915ddd896703`  
		Last Modified: Fri, 01 Apr 2022 18:24:00 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b37451ec93d4c6282ae4f1f3c0bb596a7ee8dc13e8c42744d0b5bfc819264a`  
		Last Modified: Fri, 01 Apr 2022 18:23:49 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:1dc812cf6152a1dbd7dd664e0764032b903cc57c50cff56b29cd4aca4225acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:b8b90f3f8aa8a5a5a0ec94c45447c20d7e2653088cd2f92fadc0fc1adbdfe9c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15d1ac77f073ff34cd4af6e8870392ef73eb84279d0aeb4e35641c72b1ae3d4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:34:48 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:34:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 22:35:07 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 22:35:07 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 22:35:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:09 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 22:35:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 22:35:18 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 22:35:18 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 22:35:19 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 22:35:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 22:35:19 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 22:35:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918014104c9ad49400ad5b9cc91d4bcbae82a73fa5abc7a409bf899c6c43f707`  
		Last Modified: Sat, 19 Mar 2022 22:36:36 GMT  
		Size: 93.7 MB (93654889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dbdd5fbdd128de63982a3bcd426031fd93f653efb545091ac58b78a211fe`  
		Last Modified: Sat, 19 Mar 2022 22:36:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b04accad0ea54945a94640fe15c4f18217ac339546430605562903bb6e198c`  
		Last Modified: Sat, 19 Mar 2022 22:36:23 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ddf332606cb830b506954d33ba501b217b0cf296e237e53ef52a6a9a64c442`  
		Last Modified: Sat, 19 Mar 2022 22:36:22 GMT  
		Size: 1.0 MB (1003224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212fc94ac887dd5a2399140898860c0a998fe2df050fc6e32930fee44eb331d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea58fb34b6055f277ccc1d770336f1a956999418f8c74dcac36d843e5b416d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ddcab601ff797ff8b88340a09e3597f00209e58763e8cf7ed883c7c7dcb87`  
		Last Modified: Sat, 19 Mar 2022 22:36:28 GMT  
		Size: 113.7 MB (113727937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c310e4514d6b20246d217eb5e9eb415ba672947ac5986dff90d60de6cee91c`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8145813d259caf6cd0bea5d1927b07af9b65099efde705c1b7dc4b12dc186c85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282818f0e70e12d2041d5851adc6e578279aaaed15d0a8744828bf7dc42eefed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:09:07 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:09:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 15:09:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 15:09:55 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 15:09:56 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 15:09:57 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 15:09:58 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 15:09:59 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 15:10:00 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 15:10:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 15:10:02 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 15:10:03 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 15:10:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:06 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 15:10:08 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 15:10:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 15:10:29 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 15:10:29 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 15:10:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 15:10:31 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 15:10:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3433408c5fc7f4ae638ee2b5297e626eccb6ef1eaa854483eaa88fe9452b9`  
		Last Modified: Sat, 19 Mar 2022 15:12:08 GMT  
		Size: 85.8 MB (85763156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cf766653b0804c4ca85b92cc0c0069fac5a3f16d050f228364daa9898cdddc`  
		Last Modified: Sat, 19 Mar 2022 15:11:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef7cbb4cb2bf00d122900c6fc72a76a1c4ce7e507619ce147f81ef8541dd2`  
		Last Modified: Sat, 19 Mar 2022 15:11:57 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708c338db08b4e85061950c8cb417d1fdd8d11ab132c8869662712a9d49a856`  
		Last Modified: Sat, 19 Mar 2022 15:11:55 GMT  
		Size: 929.4 KB (929409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ab77260b346ebc4ffb2b67788f195a531157a6a926db586e202224550f95b5`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a15c093ce6465bc4b31ce2c94333e202d3a124194d56bb99438c8074746c3c`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0df29d03ead5b114014be21794a723b2a019942d32b8d108fe3f1f2de09ff`  
		Last Modified: Sat, 19 Mar 2022 15:12:12 GMT  
		Size: 113.7 MB (113727850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4162cb8595bb82ce1922c26bc251eadd27b261925942c84f067f35057191`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:0c8c69d7af8f945591a5d089408490bf52d5bc01ddafc64b7143d5ec6676a8ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7996e14d3d401d9e6a086fdc28917a40774b46df8ec09f0dd2d332cf566df8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:55:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:56:02 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:56:12 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:57:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:57:03 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:57:07 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 20:57:12 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:57:15 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:57:17 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:57:19 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 20:57:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 20:57:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 20:57:25 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:57:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:36 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:57:37 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 20:57:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 20:58:01 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 20:58:07 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:58:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:58:14 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:58:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54998de650aec3ff8c87077551a8a8dedbac826f959645af516a214758030de1`  
		Last Modified: Sat, 19 Mar 2022 21:00:18 GMT  
		Size: 86.6 MB (86557500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80861eb3c1c18c4914806cea4a42cc6605837eb735445fe587096738b931ba`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e3e83293caa8f19217184082aaf48f054162fd676b0bfe80c811db04b5fa07`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e62718fccbad62107b4fe7fd7a9a97a92e26d79914dbc2cd2ce19c1ae3a3e`  
		Last Modified: Sat, 19 Mar 2022 21:00:01 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ad91e85241ec6b752c76025976f23d679c8eda783616cb3d8830044dcb21a`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaebf6593ed9f193fbd8172caa14b34ddf91ceab1a3dc48c01ad9e695794966`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d1d821c92f5f66422e0625adaed7d15289260431916f065c873a51902db85`  
		Last Modified: Sat, 19 Mar 2022 21:00:10 GMT  
		Size: 113.7 MB (113727951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730acde910ffb0b1920533e60561ebf0826b19c5d57baa84709e782722f8539`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:1dc812cf6152a1dbd7dd664e0764032b903cc57c50cff56b29cd4aca4225acd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:b8b90f3f8aa8a5a5a0ec94c45447c20d7e2653088cd2f92fadc0fc1adbdfe9c3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235101881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15d1ac77f073ff34cd4af6e8870392ef73eb84279d0aeb4e35641c72b1ae3d4`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:26 GMT
ADD file:f554512cb0acad99508554656767804e4821ece488fac0e46fd2c643a39f7021 in / 
# Fri, 18 Mar 2022 05:30:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 22:32:22 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 22:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 22:34:48 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 22:34:49 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 22:35:07 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 22:35:07 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 22:35:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 22:35:08 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 22:35:09 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 22:35:09 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 22:35:18 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 22:35:18 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 22:35:19 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 22:35:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 22:35:19 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 22:35:20 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:11323ed2c65349758e68a03a8e43825ec263dc9790daea93cf83b18ad0703109`  
		Last Modified: Thu, 17 Mar 2022 11:55:05 GMT  
		Size: 26.7 MB (26708634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918014104c9ad49400ad5b9cc91d4bcbae82a73fa5abc7a409bf899c6c43f707`  
		Last Modified: Sat, 19 Mar 2022 22:36:36 GMT  
		Size: 93.7 MB (93654889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7948dbdd5fbdd128de63982a3bcd426031fd93f653efb545091ac58b78a211fe`  
		Last Modified: Sat, 19 Mar 2022 22:36:24 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b04accad0ea54945a94640fe15c4f18217ac339546430605562903bb6e198c`  
		Last Modified: Sat, 19 Mar 2022 22:36:23 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ddf332606cb830b506954d33ba501b217b0cf296e237e53ef52a6a9a64c442`  
		Last Modified: Sat, 19 Mar 2022 22:36:22 GMT  
		Size: 1.0 MB (1003224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0212fc94ac887dd5a2399140898860c0a998fe2df050fc6e32930fee44eb331d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baea58fb34b6055f277ccc1d770336f1a956999418f8c74dcac36d843e5b416d`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 3.3 KB (3303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24ddcab601ff797ff8b88340a09e3597f00209e58763e8cf7ed883c7c7dcb87`  
		Last Modified: Sat, 19 Mar 2022 22:36:28 GMT  
		Size: 113.7 MB (113727937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c310e4514d6b20246d217eb5e9eb415ba672947ac5986dff90d60de6cee91c`  
		Last Modified: Sat, 19 Mar 2022 22:36:21 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:8145813d259caf6cd0bea5d1927b07af9b65099efde705c1b7dc4b12dc186c85
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224156613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:282818f0e70e12d2041d5851adc6e578279aaaed15d0a8744828bf7dc42eefed`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:44 GMT
ADD file:3fc0139579b748872ad588bc76190747b882f6e343893c0f6e6983542ce089b9 in / 
# Fri, 18 Mar 2022 00:40:44 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 15:06:29 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 15:09:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 15:09:07 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 15:09:08 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 15:09:54 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 15:09:55 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 15:09:56 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 15:09:57 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 15:09:58 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 15:09:59 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 15:10:00 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 15:10:01 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 15:10:02 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 15:10:03 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:04 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 15:10:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 15:10:06 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 15:10:08 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 15:10:28 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 15:10:29 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 15:10:29 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 15:10:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 15:10:31 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 15:10:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:a0bce69069710cd1ada634950a38f397db06a36de45b4132a5ca244df440bc2e`  
		Last Modified: Fri, 18 Mar 2022 00:42:18 GMT  
		Size: 23.7 MB (23729104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb3433408c5fc7f4ae638ee2b5297e626eccb6ef1eaa854483eaa88fe9452b9`  
		Last Modified: Sat, 19 Mar 2022 15:12:08 GMT  
		Size: 85.8 MB (85763156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67cf766653b0804c4ca85b92cc0c0069fac5a3f16d050f228364daa9898cdddc`  
		Last Modified: Sat, 19 Mar 2022 15:11:56 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9faef7cbb4cb2bf00d122900c6fc72a76a1c4ce7e507619ce147f81ef8541dd2`  
		Last Modified: Sat, 19 Mar 2022 15:11:57 GMT  
		Size: 1.9 KB (1863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e708c338db08b4e85061950c8cb417d1fdd8d11ab132c8869662712a9d49a856`  
		Last Modified: Sat, 19 Mar 2022 15:11:55 GMT  
		Size: 929.4 KB (929409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ab77260b346ebc4ffb2b67788f195a531157a6a926db586e202224550f95b5`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a15c093ce6465bc4b31ce2c94333e202d3a124194d56bb99438c8074746c3c`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 3.3 KB (3309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a0df29d03ead5b114014be21794a723b2a019942d32b8d108fe3f1f2de09ff`  
		Last Modified: Sat, 19 Mar 2022 15:12:12 GMT  
		Size: 113.7 MB (113727850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c4162cb8595bb82ce1922c26bc251eadd27b261925942c84f067f35057191`  
		Last Modified: Sat, 19 Mar 2022 15:11:54 GMT  
		Size: 1.7 KB (1686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:0c8c69d7af8f945591a5d089408490bf52d5bc01ddafc64b7143d5ec6676a8ad
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231634930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e7996e14d3d401d9e6a086fdc28917a40774b46df8ec09f0dd2d332cf566df8`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 18 Mar 2022 00:47:57 GMT
ADD file:512f577cb3b73f892801365276edc7835b0fbed63fe39c4e98c86264d363163b in / 
# Fri, 18 Mar 2022 00:48:04 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 20:47:36 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Sat, 19 Mar 2022 20:55:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 20:56:02 GMT
RUN mkdir /opt/custom-init.d/
# Sat, 19 Mar 2022 20:56:12 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Sat, 19 Mar 2022 20:57:00 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Sat, 19 Mar 2022 20:57:03 GMT
ARG BONITA_VERSION
# Sat, 19 Mar 2022 20:57:07 GMT
ARG BRANDING_VERSION
# Sat, 19 Mar 2022 20:57:12 GMT
ARG BONITA_SHA256
# Sat, 19 Mar 2022 20:57:15 GMT
ARG BASE_URL
# Sat, 19 Mar 2022 20:57:17 GMT
ARG BONITA_URL
# Sat, 19 Mar 2022 20:57:19 GMT
ENV BONITA_VERSION=7.13.0
# Sat, 19 Mar 2022 20:57:21 GMT
ENV BRANDING_VERSION=2021.2-u0
# Sat, 19 Mar 2022 20:57:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Sat, 19 Mar 2022 20:57:25 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:26 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Sat, 19 Mar 2022 20:57:28 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Sat, 19 Mar 2022 20:57:36 GMT
RUN mkdir /opt/files
# Sat, 19 Mar 2022 20:57:37 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Sat, 19 Mar 2022 20:57:56 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Sat, 19 Mar 2022 20:58:01 GMT
ENV HTTP_API=false
# Sat, 19 Mar 2022 20:58:07 GMT
VOLUME [/opt/bonita]
# Sat, 19 Mar 2022 20:58:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Sat, 19 Mar 2022 20:58:14 GMT
EXPOSE 8080
# Sat, 19 Mar 2022 20:58:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:37a959c2edf986d1489b0000a2dbfecd72195cde6524f2a6545bf3c5d66f6bac`  
		Last Modified: Fri, 18 Mar 2022 00:50:57 GMT  
		Size: 30.4 MB (30438056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54998de650aec3ff8c87077551a8a8dedbac826f959645af516a214758030de1`  
		Last Modified: Sat, 19 Mar 2022 21:00:18 GMT  
		Size: 86.6 MB (86557500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d80861eb3c1c18c4914806cea4a42cc6605837eb735445fe587096738b931ba`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4e3e83293caa8f19217184082aaf48f054162fd676b0bfe80c811db04b5fa07`  
		Last Modified: Sat, 19 Mar 2022 21:00:04 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:172e62718fccbad62107b4fe7fd7a9a97a92e26d79914dbc2cd2ce19c1ae3a3e`  
		Last Modified: Sat, 19 Mar 2022 21:00:01 GMT  
		Size: 904.2 KB (904217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2ad91e85241ec6b752c76025976f23d679c8eda783616cb3d8830044dcb21a`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaebf6593ed9f193fbd8172caa14b34ddf91ceab1a3dc48c01ad9e695794966`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 3.3 KB (3306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179d1d821c92f5f66422e0625adaed7d15289260431916f065c873a51902db85`  
		Last Modified: Sat, 19 Mar 2022 21:00:10 GMT  
		Size: 113.7 MB (113727951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730acde910ffb0b1920533e60561ebf0826b19c5d57baa84709e782722f8539`  
		Last Modified: Sat, 19 Mar 2022 21:00:00 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14`

```console
$ docker pull bonita@sha256:dbe41ab9ee8c3caa42cc5e1125ee8a2572faf02a4bc1c5cbedb3dbc0ddb82990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14` - linux; amd64

```console
$ docker pull bonita@sha256:72ba4fd5c5b5e75b4a4aac891e95a4a708b3fcff5448a82d44433a3e178baf60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3122e6b976281e453833fbfda09b1455e6dc94e24cdef01ca341319ace1d23c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:19:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:19:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:19:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:19:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:50 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:19:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:19:58 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:19:59 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:19:59 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:19:59 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:19:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:19:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e79f563d8aab8c0eba270cec8a016d662c148be1c254ec76d50ad5486cc1b4`  
		Last Modified: Fri, 01 Apr 2022 18:21:02 GMT  
		Size: 60.7 MB (60744597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa255d535aa1bf014e65f4e1d6b0fa40cba553688081c9a78c29b690676b93`  
		Last Modified: Fri, 01 Apr 2022 18:20:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669df2ea372e0ec60d6bea4820d349f0a3748a25ebc6819b4f93d4bcc4c8a398`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d10b61b855ba40ce63a4ca04403f7ee25ed4d8d79592e04779032096d64866`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef831ba0489b62722b56ccc4d5a24ad3e2a6928c455499930f91088a07f852dd`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9264ea8039ded28c2527884eda40ad24b08e27b1d3c9f459b889ea332fb55b92`  
		Last Modified: Fri, 01 Apr 2022 18:20:58 GMT  
		Size: 116.7 MB (116690816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9672a4c884851bccaeebbb6edcec8b9e4ef7588b0568aec71d0eac982b510851`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:50c970cdd14d323dd1c99745ae3925ba8208a92c9042696bae707a54b14517e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0918abc89121ebb476786f81746682254ced77a57c4cfc7739ce22ff513a8de`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 17:40:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 17:40:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 17:40:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 17:40:51 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:52 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:53 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:54 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:55 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:56 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 17:40:57 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 17:40:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 17:40:59 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:41:01 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:02 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:41:04 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 17:41:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 17:41:12 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 17:41:13 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 17:41:14 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 17:41:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 17:41:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 17:41:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 17:41:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 17:41:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 17:41:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 17:41:21 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 17:41:22 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 17:41:23 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 17:41:24 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 17:41:26 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 17:41:26 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 17:41:27 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 17:41:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4f822664704f6f79949aefca413d12eb17df87a9aadd95325020d1a6a9b9b`  
		Last Modified: Fri, 01 Apr 2022 17:43:02 GMT  
		Size: 60.1 MB (60067359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c616b6eca14fdd3df9fc774463c6ab0e906bfe7cdce04ce4da0818a5efd5a6`  
		Last Modified: Fri, 01 Apr 2022 17:42:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2d80d2d31fe74211a2e1feb10facc69bccfb5545f85f445b8bd901fed497f`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ce5132c23db90ca4ba8609f07532a889517754b7497ce4cf02a58a49c6b11`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5f63b232f4b68842b3891c68aeae172a15809c56a149747b5e88a78ba793cc`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 3.0 KB (2998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1c56ddddc60c65d81eea0ab6a218f73a0a2bbd1f1a2dc46dafa1a20df5e696`  
		Last Modified: Fri, 01 Apr 2022 17:43:04 GMT  
		Size: 116.7 MB (116688763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a3aab75707fb0e9f2cae8205a791a83ccfdfa51d46f778107d78fd2531e59d`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14` - linux; ppc64le

```console
$ docker pull bonita@sha256:4eafff51214222baf590717b558ab80c9e3b3dc89ecf9fb95af96e0b4277ecf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176074668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e45f2da93ca22ec79676dbdf673af55a554f680e979a353255374346ddadb8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:16:52 GMT
ADD file:9e7b65a431d59070abaadae56d9c3fc59c899af881939e4353b1f524b2bd5185 in / 
# Tue, 29 Mar 2022 00:16:55 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:20:17 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:20:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:20:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:20:43 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:20:46 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:20:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:20:50 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:20:52 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:20:54 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:20:56 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:20:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:21:01 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:21:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:19 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:21:20 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:21:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:21:50 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:21:57 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:22:02 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:22:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:22:10 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:22:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:22:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:22:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:22:21 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:22:25 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:22:33 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:22:39 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:22:45 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:22:48 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:22:50 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:22:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:23:04 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1c611bca4fa49cac5bc1e3826ad53fee85ed659d24bffcccd86c3f04be07339a`  
		Last Modified: Tue, 29 Mar 2022 00:18:26 GMT  
		Size: 2.8 MB (2811009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c49f5b4939e43318833abc91f2f281812dd7be534bc1abc9b5c00bdff8592d0`  
		Last Modified: Fri, 01 Apr 2022 18:24:33 GMT  
		Size: 56.6 MB (56562818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68fd31f2119b8e80ee813acd91a33add2bb6ca795a12816046c44571cca10ff`  
		Last Modified: Fri, 01 Apr 2022 18:24:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac3c3ae00e0450c3436310816fa5a5c2a5a0d7d6a7f6db788bf73d2f22a02f9`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3a61437e3af23539f3a2e0826774e6e4055fd807f5c1f7468d6121b852fc04`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70757e12053925c257cca583ad4bd53f04208ab8b8726a85dcf5152bba7542c1`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 3.0 KB (3038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cf4564c5e52458dca4281258184644faa08ab0e5097bbe95ba7c8feab3aba4`  
		Last Modified: Fri, 01 Apr 2022 18:24:30 GMT  
		Size: 116.7 MB (116690818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17eda15dd05eb4b902ea75e5e95dec04a448b4c1ebe78d3c29374b9e7a93486`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.14.0`

```console
$ docker pull bonita@sha256:dbe41ab9ee8c3caa42cc5e1125ee8a2572faf02a4bc1c5cbedb3dbc0ddb82990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.14.0` - linux; amd64

```console
$ docker pull bonita@sha256:72ba4fd5c5b5e75b4a4aac891e95a4a708b3fcff5448a82d44433a3e178baf60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3122e6b976281e453833fbfda09b1455e6dc94e24cdef01ca341319ace1d23c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:19:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:19:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:19:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:19:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:50 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:19:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:19:58 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:19:59 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:19:59 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:19:59 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:19:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:19:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e79f563d8aab8c0eba270cec8a016d662c148be1c254ec76d50ad5486cc1b4`  
		Last Modified: Fri, 01 Apr 2022 18:21:02 GMT  
		Size: 60.7 MB (60744597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa255d535aa1bf014e65f4e1d6b0fa40cba553688081c9a78c29b690676b93`  
		Last Modified: Fri, 01 Apr 2022 18:20:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669df2ea372e0ec60d6bea4820d349f0a3748a25ebc6819b4f93d4bcc4c8a398`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d10b61b855ba40ce63a4ca04403f7ee25ed4d8d79592e04779032096d64866`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef831ba0489b62722b56ccc4d5a24ad3e2a6928c455499930f91088a07f852dd`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9264ea8039ded28c2527884eda40ad24b08e27b1d3c9f459b889ea332fb55b92`  
		Last Modified: Fri, 01 Apr 2022 18:20:58 GMT  
		Size: 116.7 MB (116690816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9672a4c884851bccaeebbb6edcec8b9e4ef7588b0568aec71d0eac982b510851`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:50c970cdd14d323dd1c99745ae3925ba8208a92c9042696bae707a54b14517e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0918abc89121ebb476786f81746682254ced77a57c4cfc7739ce22ff513a8de`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 17:40:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 17:40:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 17:40:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 17:40:51 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:52 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:53 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:54 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:55 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:56 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 17:40:57 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 17:40:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 17:40:59 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:41:01 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:02 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:41:04 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 17:41:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 17:41:12 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 17:41:13 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 17:41:14 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 17:41:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 17:41:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 17:41:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 17:41:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 17:41:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 17:41:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 17:41:21 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 17:41:22 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 17:41:23 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 17:41:24 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 17:41:26 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 17:41:26 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 17:41:27 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 17:41:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4f822664704f6f79949aefca413d12eb17df87a9aadd95325020d1a6a9b9b`  
		Last Modified: Fri, 01 Apr 2022 17:43:02 GMT  
		Size: 60.1 MB (60067359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c616b6eca14fdd3df9fc774463c6ab0e906bfe7cdce04ce4da0818a5efd5a6`  
		Last Modified: Fri, 01 Apr 2022 17:42:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2d80d2d31fe74211a2e1feb10facc69bccfb5545f85f445b8bd901fed497f`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ce5132c23db90ca4ba8609f07532a889517754b7497ce4cf02a58a49c6b11`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5f63b232f4b68842b3891c68aeae172a15809c56a149747b5e88a78ba793cc`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 3.0 KB (2998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1c56ddddc60c65d81eea0ab6a218f73a0a2bbd1f1a2dc46dafa1a20df5e696`  
		Last Modified: Fri, 01 Apr 2022 17:43:04 GMT  
		Size: 116.7 MB (116688763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a3aab75707fb0e9f2cae8205a791a83ccfdfa51d46f778107d78fd2531e59d`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.14.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:4eafff51214222baf590717b558ab80c9e3b3dc89ecf9fb95af96e0b4277ecf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176074668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e45f2da93ca22ec79676dbdf673af55a554f680e979a353255374346ddadb8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:16:52 GMT
ADD file:9e7b65a431d59070abaadae56d9c3fc59c899af881939e4353b1f524b2bd5185 in / 
# Tue, 29 Mar 2022 00:16:55 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:20:17 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:20:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:20:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:20:43 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:20:46 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:20:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:20:50 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:20:52 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:20:54 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:20:56 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:20:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:21:01 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:21:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:19 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:21:20 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:21:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:21:50 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:21:57 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:22:02 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:22:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:22:10 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:22:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:22:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:22:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:22:21 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:22:25 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:22:33 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:22:39 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:22:45 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:22:48 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:22:50 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:22:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:23:04 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1c611bca4fa49cac5bc1e3826ad53fee85ed659d24bffcccd86c3f04be07339a`  
		Last Modified: Tue, 29 Mar 2022 00:18:26 GMT  
		Size: 2.8 MB (2811009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c49f5b4939e43318833abc91f2f281812dd7be534bc1abc9b5c00bdff8592d0`  
		Last Modified: Fri, 01 Apr 2022 18:24:33 GMT  
		Size: 56.6 MB (56562818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68fd31f2119b8e80ee813acd91a33add2bb6ca795a12816046c44571cca10ff`  
		Last Modified: Fri, 01 Apr 2022 18:24:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac3c3ae00e0450c3436310816fa5a5c2a5a0d7d6a7f6db788bf73d2f22a02f9`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3a61437e3af23539f3a2e0826774e6e4055fd807f5c1f7468d6121b852fc04`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70757e12053925c257cca583ad4bd53f04208ab8b8726a85dcf5152bba7542c1`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 3.0 KB (3038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cf4564c5e52458dca4281258184644faa08ab0e5097bbe95ba7c8feab3aba4`  
		Last Modified: Fri, 01 Apr 2022 18:24:30 GMT  
		Size: 116.7 MB (116690818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17eda15dd05eb4b902ea75e5e95dec04a448b4c1ebe78d3c29374b9e7a93486`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:dbe41ab9ee8c3caa42cc5e1125ee8a2572faf02a4bc1c5cbedb3dbc0ddb82990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:72ba4fd5c5b5e75b4a4aac891e95a4a708b3fcff5448a82d44433a3e178baf60
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.3 MB (180259949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3122e6b976281e453833fbfda09b1455e6dc94e24cdef01ca341319ace1d23c`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:43 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:19:47 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:19:48 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:19:48 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:19:48 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:19:49 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:19:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:19:50 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:19:50 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:19:57 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:19:58 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:19:58 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:19:58 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:19:58 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:19:59 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:19:59 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:19:59 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:19:59 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:19:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:19:59 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e79f563d8aab8c0eba270cec8a016d662c148be1c254ec76d50ad5486cc1b4`  
		Last Modified: Fri, 01 Apr 2022 18:21:02 GMT  
		Size: 60.7 MB (60744597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16aa255d535aa1bf014e65f4e1d6b0fa40cba553688081c9a78c29b690676b93`  
		Last Modified: Fri, 01 Apr 2022 18:20:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:669df2ea372e0ec60d6bea4820d349f0a3748a25ebc6819b4f93d4bcc4c8a398`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d10b61b855ba40ce63a4ca04403f7ee25ed4d8d79592e04779032096d64866`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef831ba0489b62722b56ccc4d5a24ad3e2a6928c455499930f91088a07f852dd`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 3.0 KB (3036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9264ea8039ded28c2527884eda40ad24b08e27b1d3c9f459b889ea332fb55b92`  
		Last Modified: Fri, 01 Apr 2022 18:20:58 GMT  
		Size: 116.7 MB (116690816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9672a4c884851bccaeebbb6edcec8b9e4ef7588b0568aec71d0eac982b510851`  
		Last Modified: Fri, 01 Apr 2022 18:20:51 GMT  
		Size: 5.4 KB (5424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:50c970cdd14d323dd1c99745ae3925ba8208a92c9042696bae707a54b14517e6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **179.5 MB (179482328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0918abc89121ebb476786f81746682254ced77a57c4cfc7739ce22ff513a8de`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:40:05 GMT
ADD file:24e8b04304ef91bbf949674909ccaf2c66e3dcd096c3c307a0510569eadf576f in / 
# Tue, 29 Mar 2022 00:40:05 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 17:40:46 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 17:40:49 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 17:40:49 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 17:40:50 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 17:40:51 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 17:40:52 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 17:40:53 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 17:40:54 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 17:40:55 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 17:40:56 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 17:40:57 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 17:40:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 17:40:59 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:00 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 17:41:01 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 17:41:02 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 17:41:04 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 17:41:12 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 17:41:12 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 17:41:13 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 17:41:14 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 17:41:15 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 17:41:16 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 17:41:17 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 17:41:18 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 17:41:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 17:41:20 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 17:41:21 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 17:41:22 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 17:41:23 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 17:41:24 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 17:41:26 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 17:41:26 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 17:41:27 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 17:41:28 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:80fa7f07ec7b717ec5f8e2717b91e3d659e129052ec3def2570a5674322688d9`  
		Last Modified: Tue, 29 Mar 2022 00:41:08 GMT  
		Size: 2.7 MB (2716347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc4f822664704f6f79949aefca413d12eb17df87a9aadd95325020d1a6a9b9b`  
		Last Modified: Fri, 01 Apr 2022 17:43:02 GMT  
		Size: 60.1 MB (60067359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c616b6eca14fdd3df9fc774463c6ab0e906bfe7cdce04ce4da0818a5efd5a6`  
		Last Modified: Fri, 01 Apr 2022 17:42:54 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe2d80d2d31fe74211a2e1feb10facc69bccfb5545f85f445b8bd901fed497f`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ce5132c23db90ca4ba8609f07532a889517754b7497ce4cf02a58a49c6b11`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5f63b232f4b68842b3891c68aeae172a15809c56a149747b5e88a78ba793cc`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 3.0 KB (2998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1c56ddddc60c65d81eea0ab6a218f73a0a2bbd1f1a2dc46dafa1a20df5e696`  
		Last Modified: Fri, 01 Apr 2022 17:43:04 GMT  
		Size: 116.7 MB (116688763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a3aab75707fb0e9f2cae8205a791a83ccfdfa51d46f778107d78fd2531e59d`  
		Last Modified: Fri, 01 Apr 2022 17:42:51 GMT  
		Size: 5.4 KB (5392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:4eafff51214222baf590717b558ab80c9e3b3dc89ecf9fb95af96e0b4277ecf3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.1 MB (176074668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e45f2da93ca22ec79676dbdf673af55a554f680e979a353255374346ddadb8`
-	Entrypoint: `["\/opt\/files\/startup.sh"]`
-	Default Command: `["\/opt\/bonita\/server\/bin\/catalina.sh","run"]`

```dockerfile
# Tue, 29 Mar 2022 00:16:52 GMT
ADD file:9e7b65a431d59070abaadae56d9c3fc59c899af881939e4353b1f524b2bd5185 in / 
# Tue, 29 Mar 2022 00:16:55 GMT
CMD ["/bin/sh"]
# Fri, 01 Apr 2022 18:19:49 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Apr 2022 18:20:17 GMT
RUN apk add --no-cache curl unzip bash su-exec jattach openjdk11-jre-headless
# Fri, 01 Apr 2022 18:20:29 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Apr 2022 18:20:39 GMT
RUN addgroup -S -g 1000 bonita  && adduser -u 1000 -S  -G bonita -h /opt/bonita/ -s /sbin/nologin  bonita
# Fri, 01 Apr 2022 18:20:43 GMT
ARG BONITA_VERSION
# Fri, 01 Apr 2022 18:20:46 GMT
ARG BRANDING_VERSION
# Fri, 01 Apr 2022 18:20:48 GMT
ARG BONITA_SHA256
# Fri, 01 Apr 2022 18:20:50 GMT
ARG BASE_URL
# Fri, 01 Apr 2022 18:20:52 GMT
ARG BONITA_URL
# Fri, 01 Apr 2022 18:20:54 GMT
ENV BONITA_VERSION=7.14.0
# Fri, 01 Apr 2022 18:20:56 GMT
ENV BRANDING_VERSION=2022.1-u0
# Fri, 01 Apr 2022 18:20:58 GMT
ENV BONITA_SHA256=a88b3f4368bd68dda4eccf4680a71b7e523678811b6b3bcd61cd85e67e9b9aeb
# Fri, 01 Apr 2022 18:21:01 GMT
ENV ZIP_FILE=BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:03 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Apr 2022 18:21:06 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2022.1-u0/BonitaCommunity-2022.1-u0.zip
# Fri, 01 Apr 2022 18:21:19 GMT
RUN mkdir /opt/files
# Fri, 01 Apr 2022 18:21:20 GMT
COPY dir:55abb36f42ed7e3d3197415cf20ab2abe54eeefc3accbc7bc3be8dbd2d0f8d41 in /opt/files 
# Fri, 01 Apr 2022 18:21:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && echo "$BONITA_SHA256 */opt/files/$ZIP_FILE" | sha256sum -c - ; fi   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && mv /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/* /opt/bonita   && rmdir /opt/bonita/BonitaCommunity-${BRANDING_VERSION}   && unzip /opt/bonita/server/webapps/bonita.war -d /opt/bonita/server/webapps/bonita/   && rm /opt/bonita/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip   && mkdir -p /opt/bonita/conf/logs/   && mkdir -p /opt/bonita/logs/   && mv /opt/files/log4j2/log4j2-appenders.xml /opt/bonita/conf/logs/   && mv /opt/bonita/server/conf/log4j2-loggers.xml /opt/bonita/conf/logs/   && chown -R bonita:bonita /opt/bonita   && chmod go+w /opt/   && chmod -R +rX /opt   && chmod go+w /opt/bonita   && chmod 777 /opt/bonita/server/logs   && chmod 777 /opt/bonita/logs/   && chmod 777 /opt/bonita/server/temp   && chmod 777 /opt/bonita/server/work   && chmod -R go+w /opt/bonita/server/conf   && chmod -R go+w /opt/bonita/server/bin   && chmod -R go+w /opt/bonita/server/lib/bonita   && chmod -R go+w /opt/bonita/setup
# Fri, 01 Apr 2022 18:21:50 GMT
ENV HTTP_API=false
# Fri, 01 Apr 2022 18:21:57 GMT
ENV HTTP_API_USERNAME=http-api
# Fri, 01 Apr 2022 18:22:02 GMT
ENV HTTP_API_PASSWORD=
# Fri, 01 Apr 2022 18:22:06 GMT
ENV MONITORING_USERNAME=monitoring
# Fri, 01 Apr 2022 18:22:10 GMT
ENV MONITORING_PASSWORD=mon1tor1ng_adm1n
# Fri, 01 Apr 2022 18:22:13 GMT
ENV JMX_REMOTE_ACCESS=false
# Fri, 01 Apr 2022 18:22:16 GMT
ENV REMOTE_IP_VALVE_ENABLED=false
# Fri, 01 Apr 2022 18:22:19 GMT
ENV ACCESSLOGS_STDOUT_ENABLED=false
# Fri, 01 Apr 2022 18:22:21 GMT
ENV ACCESSLOGS_FILES_ENABLED=false
# Fri, 01 Apr 2022 18:22:25 GMT
ENV ACCESSLOGS_PATH=/opt/bonita/logs
# Fri, 01 Apr 2022 18:22:33 GMT
ENV ACCESSLOGS_PATH_APPEND_HOSTNAME=false
# Fri, 01 Apr 2022 18:22:39 GMT
ENV ACCESSLOGS_MAX_DAYS=30
# Fri, 01 Apr 2022 18:22:45 GMT
ENV HTTP_MAX_THREADS=20
# Fri, 01 Apr 2022 18:22:48 GMT
COPY dir:ad0fdf5900d3b914efcbba3170cc7d773b5d57072eba969a052457514aa27adc in /opt/templates 
# Fri, 01 Apr 2022 18:22:50 GMT
EXPOSE 8080 9000
# Fri, 01 Apr 2022 18:22:59 GMT
ENTRYPOINT ["/opt/files/startup.sh"]
# Fri, 01 Apr 2022 18:23:04 GMT
CMD ["/opt/bonita/server/bin/catalina.sh" "run"]
```

-	Layers:
	-	`sha256:1c611bca4fa49cac5bc1e3826ad53fee85ed659d24bffcccd86c3f04be07339a`  
		Last Modified: Tue, 29 Mar 2022 00:18:26 GMT  
		Size: 2.8 MB (2811009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c49f5b4939e43318833abc91f2f281812dd7be534bc1abc9b5c00bdff8592d0`  
		Last Modified: Fri, 01 Apr 2022 18:24:33 GMT  
		Size: 56.6 MB (56562818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68fd31f2119b8e80ee813acd91a33add2bb6ca795a12816046c44571cca10ff`  
		Last Modified: Fri, 01 Apr 2022 18:24:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac3c3ae00e0450c3436310816fa5a5c2a5a0d7d6a7f6db788bf73d2f22a02f9`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3a61437e3af23539f3a2e0826774e6e4055fd807f5c1f7468d6121b852fc04`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70757e12053925c257cca583ad4bd53f04208ab8b8726a85dcf5152bba7542c1`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 3.0 KB (3038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cf4564c5e52458dca4281258184644faa08ab0e5097bbe95ba7c8feab3aba4`  
		Last Modified: Fri, 01 Apr 2022 18:24:30 GMT  
		Size: 116.7 MB (116690818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a17eda15dd05eb4b902ea75e5e95dec04a448b4c1ebe78d3c29374b9e7a93486`  
		Last Modified: Fri, 01 Apr 2022 18:24:19 GMT  
		Size: 5.4 KB (5422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
