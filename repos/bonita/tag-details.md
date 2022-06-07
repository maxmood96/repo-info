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
$ docker pull bonita@sha256:7c4f89e1a1c71329633982be8af74bdaec5fd465bebd1cfc3ca3d9996c07293b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:b3d60108d31746ac6b0a250ae5a1584f9c5feb1dbde7a14b7be51ee2d25c9677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237346125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f5d5bedf104280789d1778c459816bba7d492f11c51cd0c75785c2ca77d3dc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:53:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 06 Jun 2022 23:54:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 23:54:17 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 06 Jun 2022 23:54:17 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 06 Jun 2022 23:54:20 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BONITA_VERSION
# Mon, 06 Jun 2022 23:54:39 GMT
ARG BRANDING_VERSION
# Mon, 06 Jun 2022 23:54:39 GMT
ARG BONITA_SHA256
# Mon, 06 Jun 2022 23:54:39 GMT
ARG BASE_URL
# Mon, 06 Jun 2022 23:54:40 GMT
ARG BONITA_URL
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 06 Jun 2022 23:54:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 06 Jun 2022 23:54:41 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 06 Jun 2022 23:54:41 GMT
RUN mkdir /opt/files
# Mon, 06 Jun 2022 23:54:41 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 06 Jun 2022 23:54:50 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 06 Jun 2022 23:54:52 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 06 Jun 2022 23:54:53 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 06 Jun 2022 23:54:53 GMT
VOLUME [/opt/bonita]
# Mon, 06 Jun 2022 23:54:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 06 Jun 2022 23:54:53 GMT
EXPOSE 8080
# Mon, 06 Jun 2022 23:54:53 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5418a805118d48622924b6aafd90b6d0fd41a00a2afcb8573edae873ad6b34`  
		Last Modified: Mon, 06 Jun 2022 23:56:08 GMT  
		Size: 93.7 MB (93701902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebb439837c2100d990d18cf836fa05055e32fd2bdd47a14fafc56564be51aa`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7653bdf398cf2fea20e659373f67f4403ad79ba2bc386834784dcf81a6f22b`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed9d5128126c39997f43cfed11e39f999bb3e5dc68cc31cce7ec17a24c9f99`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5561b5cdb8e81171f8ee8e8cf79d43e8ca90f682045252d97da3e8b342da0c`  
		Last Modified: Mon, 06 Jun 2022 23:56:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b1e69431891ab97af4b6be65a109d9dd07fed3c1d3e1c9feff6e32e84d408e`  
		Last Modified: Mon, 06 Jun 2022 23:56:18 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419207b701157759dda6e80cb1d11230516c456e02a170a509e6a2f807a2e41`  
		Last Modified: Mon, 06 Jun 2022 23:56:23 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d0fd575eecb3ac1fd07bf640b251c18acba86b6dbbe620f052072e37845462`  
		Last Modified: Mon, 06 Jun 2022 23:56:18 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c146fc722b92c15bb4d66f80cd54795c1097312882641b94b14c0d39cd735d71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226459583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a34adb98477ca9f8e45e840592d9d5df5bf8491e4adf0b2e471ec80372035e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:36:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 04:36:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 04:37:00 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 04:37:01 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 04:37:05 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 04:37:06 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 04:37:36 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 04:37:37 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 04:37:38 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 04:37:39 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 04:37:40 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 07 Jun 2022 04:37:41 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 07 Jun 2022 04:37:42 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 07 Jun 2022 04:37:43 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 04:37:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 04:37:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 04:37:46 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 04:37:47 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 04:37:49 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 07 Jun 2022 04:37:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 07 Jun 2022 04:38:00 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 04:38:02 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 04:38:02 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 04:38:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 04:38:04 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 04:38:05 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38187bb0cb1b93156315bff2294d1f517eee8c1d07300ab33d2453b96dce44b8`  
		Last Modified: Tue, 07 Jun 2022 04:40:03 GMT  
		Size: 85.8 MB (85823061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f02956b16c6742ce9547c2690d9faf5a1ba2b8b0638890a467c728ed26262c3`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5c77638ac3681fd4230f8794542276a7d5ed539a3696f7766ac5eed4290cec`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de196c1ba37cbc23fccaf116fef01edf217eb86d5ccd722c8669491021200dc`  
		Last Modified: Tue, 07 Jun 2022 04:39:49 GMT  
		Size: 475.8 KB (475763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed2fbaa18fc80b7a55fab9e966653d48bb94b52f47cfd33563b15aee52acfbb`  
		Last Modified: Tue, 07 Jun 2022 04:40:15 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92060965857675ec3f90ee8d339a56e4494c0c5f2fc1e7204e923ffa9a01582`  
		Last Modified: Tue, 07 Jun 2022 04:40:15 GMT  
		Size: 6.9 KB (6917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e974e1fc9a3b22f57f88118b5ab8c9031fcdcb9b6ba8f2a082eb8b1268f669bd`  
		Last Modified: Tue, 07 Jun 2022 04:40:28 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f617b62b56fdf2ca59df149c7258fc5dfe4cd6b78244eda3418f811c5ab13`  
		Last Modified: Tue, 07 Jun 2022 04:40:15 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:b56b3ae5fd5e336c93594767ecae7a32026f87bf5ffd09a13f55c8d45123f978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233951178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9fec1db19fcffd6ebef6c9cae4f880271ccbbfa9600fc7146eeb41f40158d6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:06:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 10:08:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:08:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 10:08:26 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 10:08:38 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 10:08:42 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 10:10:29 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 10:10:30 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 10:10:32 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 10:10:35 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 10:10:38 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 07 Jun 2022 10:10:41 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 07 Jun 2022 10:10:44 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 07 Jun 2022 10:10:46 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 10:10:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 10:10:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 10:10:55 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 10:11:01 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 10:11:02 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 07 Jun 2022 10:11:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 07 Jun 2022 10:11:19 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 10:11:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 10:11:30 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 10:11:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 10:11:33 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 10:11:36 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5932cab289b2b2a387d18cfb709811f1a652f05e78ced57c596e0e3a7136ca8f`  
		Last Modified: Tue, 07 Jun 2022 10:16:56 GMT  
		Size: 86.6 MB (86606720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e99318a085a88c3b7eefb71e0fb1851bbc6f00b8b9b350cd5f611e0e3294356`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128478c35447ca89ff14fbf5c1a1a2936a18e0012a7f08f2db12e421b6d46159`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4873185aa919a50c4fad4b47828805af6df63bc92c8143b5268a777fade09b6`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 475.3 KB (475347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eceaedc2b9083c2b4baf061ec3fad71b09f51e83d5e7ae2b07aa70e01bc60d3`  
		Last Modified: Tue, 07 Jun 2022 10:17:09 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba561c4766c632072d54ee899d6956320cc379ead197e70321d06a5936402f0c`  
		Last Modified: Tue, 07 Jun 2022 10:17:09 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b5afedaeef8dad41a823655dbe702900e9f84fbb2f98bbf9f560534a33c0c9`  
		Last Modified: Tue, 07 Jun 2022 10:17:22 GMT  
		Size: 116.4 MB (116415403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56f59b30a77def4359279676b77dc14e03c625eb67a39ae191af44d2125d0f`  
		Last Modified: Tue, 07 Jun 2022 10:17:09 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2`

```console
$ docker pull bonita@sha256:cb21f182992224f7d03dba6e5ee6a579d411f48a18fb16f40c492487b5fa4b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2` - linux; amd64

```console
$ docker pull bonita@sha256:ee74276139bf7c8a87f356b14edb98fa6bad507ff9a372aa1c605cada4649f3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235082013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ac44f6589b4a64d0ed54d539632fd9198c6e5d28d636d341ede8cf4325d306`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:53:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 06 Jun 2022 23:55:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 23:55:18 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 06 Jun 2022 23:55:18 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 06 Jun 2022 23:55:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BONITA_VERSION
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BRANDING_VERSION
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BONITA_SHA256
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BASE_URL
# Mon, 06 Jun 2022 23:55:22 GMT
ARG BONITA_URL
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_VERSION=7.13.0
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BRANDING_VERSION=2021.2-u0
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Mon, 06 Jun 2022 23:55:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Mon, 06 Jun 2022 23:55:23 GMT
RUN mkdir /opt/files
# Mon, 06 Jun 2022 23:55:23 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Mon, 06 Jun 2022 23:55:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Mon, 06 Jun 2022 23:55:32 GMT
ENV HTTP_API=false
# Mon, 06 Jun 2022 23:55:32 GMT
VOLUME [/opt/bonita]
# Mon, 06 Jun 2022 23:55:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 06 Jun 2022 23:55:33 GMT
EXPOSE 8080
# Mon, 06 Jun 2022 23:55:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1e67ee570f875ac56d020bb9ba2048a4b6afe001f2abf27cfcddb94522850b`  
		Last Modified: Mon, 06 Jun 2022 23:56:51 GMT  
		Size: 93.7 MB (93704786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c799895347844414e50219a00d72f2823de2835c43da6467690a7dfd8092c060`  
		Last Modified: Mon, 06 Jun 2022 23:56:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c498ca5f2196c619a41699208691a92297201323322f46a997527f30a6f4b`  
		Last Modified: Mon, 06 Jun 2022 23:56:38 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2f7a93399ccd26ef9ccf374b0aa06222a048a869aafe199d501d1502d94dd5`  
		Last Modified: Mon, 06 Jun 2022 23:56:37 GMT  
		Size: 930.5 KB (930477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e210e87ebbe93c80e1d898c2ed2ebdc54aca26d7a6a717cf3aa099924d61d90`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae012376ae09d981dd1cd1f1f85c7ebb4ee0e6045eb0e5db987a76209838f69f`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065a8420959a3c31f08f22599784d93334ea42cfe102e8096372ce3535b744ca`  
		Last Modified: Mon, 06 Jun 2022 23:56:42 GMT  
		Size: 113.7 MB (113727928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218765ecdc92ddbb127c4fa8d00d71deeb947040f31ef34ddec95ea7cbe23676`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:32ac0f06eb8208c29dcd8f48b6b5120f4a09c7d1986eea12c160e49f1f304d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224152225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a8d50a9b72b5d372fa2d247359ea8c16eeb9a96422b4c8639ebcd07516e652`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:36:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 04:38:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 04:38:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 04:38:37 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 04:38:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 04:38:41 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 04:38:42 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 04:38:43 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 04:38:44 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 04:38:45 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 04:38:46 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 07 Jun 2022 04:38:47 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 07 Jun 2022 04:38:48 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 07 Jun 2022 04:38:49 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 04:38:50 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 04:38:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 04:38:52 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 04:38:54 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 07 Jun 2022 04:39:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 07 Jun 2022 04:39:03 GMT
ENV HTTP_API=false
# Tue, 07 Jun 2022 04:39:04 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 04:39:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 04:39:06 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 04:39:07 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90c2e8ebba1a8c8c808dc0fc6713296767a6225346074a494da934e5eb1bffe`  
		Last Modified: Tue, 07 Jun 2022 04:40:58 GMT  
		Size: 85.8 MB (85823076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f858118dd99d6115eb2738eae4edbabda7fcd72b175c8bbb4f39e84e990b38f`  
		Last Modified: Tue, 07 Jun 2022 04:40:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cdd70aa503c2012f6c338f499d198c1fb27d4877f434e6b236fe78ea2f603c`  
		Last Modified: Tue, 07 Jun 2022 04:40:46 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d206c9b11ef37af5da73286104d4d2fdc9c84521778888387ddeb57ff9e1452a`  
		Last Modified: Tue, 07 Jun 2022 04:40:45 GMT  
		Size: 859.5 KB (859531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a211292cefd1b6fa526ab765b315d54614b40a4c920cc6bd223dab23fbb99fc`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf469e907a3e246b0344a753c7c4e926f314e4ee5f49009d76b06cee65b0f93`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d9c7e13abd4a2911c642e9eb0b206f5d366c496d20c9b7db27f11e69b1ab3a`  
		Last Modified: Tue, 07 Jun 2022 04:40:54 GMT  
		Size: 113.7 MB (113727876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3009fa1d28a134141a124574334d55f7cd7c043cab361fd58e9e35ef6439eeb`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2` - linux; ppc64le

```console
$ docker pull bonita@sha256:b60dcfbbd19ee916cfe82496a0a3ec32704fb02d7ef614a462a8c26b419f33ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231616671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5c514531c3d593534bda4827d79ab938f9b69604af9911b69e50720c9c5a6c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:06:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 10:14:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:14:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 10:14:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 10:14:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 10:14:35 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 10:14:37 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 10:14:42 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 10:14:44 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 10:14:46 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 10:14:50 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 07 Jun 2022 10:14:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 07 Jun 2022 10:14:57 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 07 Jun 2022 10:15:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 10:15:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 10:15:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 10:15:14 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 10:15:15 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 07 Jun 2022 10:15:32 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 07 Jun 2022 10:15:36 GMT
ENV HTTP_API=false
# Tue, 07 Jun 2022 10:15:42 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 10:15:45 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 10:15:51 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 10:15:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a331e660ead68d382742f61a8656c41551cb44956552a658c4a7b744bface060`  
		Last Modified: Tue, 07 Jun 2022 10:17:56 GMT  
		Size: 86.6 MB (86607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213b14ccc59baf8fae328306aad1c663e545d1071ae41070ca2f4b8407c3ce1`  
		Last Modified: Tue, 07 Jun 2022 10:17:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849223db8c9360d39904a129a16fcab82cc75ed0440f6b216c84181e8eaf3a9d`  
		Last Modified: Tue, 07 Jun 2022 10:17:41 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cbc038830160e8447b4c94a591d38b99d4212b0cf63674dc8d0512708ccc57`  
		Last Modified: Tue, 07 Jun 2022 10:17:39 GMT  
		Size: 831.6 KB (831568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b68ec78a742cf1aa2513ae7a692d0fe38f63e39b8360ae6358423caa08434`  
		Last Modified: Tue, 07 Jun 2022 10:17:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa847ac20a1fea971cba2a4054299001b79527c44c7aee950a97916aa8a7bfb`  
		Last Modified: Tue, 07 Jun 2022 10:17:38 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a42bd5762b185dffd9c65896d1caace35c218bc37c33dc07dd6f212844fbcb1`  
		Last Modified: Tue, 07 Jun 2022 10:17:49 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b94e67f1cc5eec539069c00057c5a4de04b37c4fd1b7077caca27601fc9b130`  
		Last Modified: Tue, 07 Jun 2022 10:17:38 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:2021.2-u0`

```console
$ docker pull bonita@sha256:cb21f182992224f7d03dba6e5ee6a579d411f48a18fb16f40c492487b5fa4b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.2-u0` - linux; amd64

```console
$ docker pull bonita@sha256:ee74276139bf7c8a87f356b14edb98fa6bad507ff9a372aa1c605cada4649f3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235082013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ac44f6589b4a64d0ed54d539632fd9198c6e5d28d636d341ede8cf4325d306`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:53:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 06 Jun 2022 23:55:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 23:55:18 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 06 Jun 2022 23:55:18 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 06 Jun 2022 23:55:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BONITA_VERSION
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BRANDING_VERSION
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BONITA_SHA256
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BASE_URL
# Mon, 06 Jun 2022 23:55:22 GMT
ARG BONITA_URL
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_VERSION=7.13.0
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BRANDING_VERSION=2021.2-u0
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Mon, 06 Jun 2022 23:55:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Mon, 06 Jun 2022 23:55:23 GMT
RUN mkdir /opt/files
# Mon, 06 Jun 2022 23:55:23 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Mon, 06 Jun 2022 23:55:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Mon, 06 Jun 2022 23:55:32 GMT
ENV HTTP_API=false
# Mon, 06 Jun 2022 23:55:32 GMT
VOLUME [/opt/bonita]
# Mon, 06 Jun 2022 23:55:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 06 Jun 2022 23:55:33 GMT
EXPOSE 8080
# Mon, 06 Jun 2022 23:55:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1e67ee570f875ac56d020bb9ba2048a4b6afe001f2abf27cfcddb94522850b`  
		Last Modified: Mon, 06 Jun 2022 23:56:51 GMT  
		Size: 93.7 MB (93704786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c799895347844414e50219a00d72f2823de2835c43da6467690a7dfd8092c060`  
		Last Modified: Mon, 06 Jun 2022 23:56:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c498ca5f2196c619a41699208691a92297201323322f46a997527f30a6f4b`  
		Last Modified: Mon, 06 Jun 2022 23:56:38 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2f7a93399ccd26ef9ccf374b0aa06222a048a869aafe199d501d1502d94dd5`  
		Last Modified: Mon, 06 Jun 2022 23:56:37 GMT  
		Size: 930.5 KB (930477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e210e87ebbe93c80e1d898c2ed2ebdc54aca26d7a6a717cf3aa099924d61d90`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae012376ae09d981dd1cd1f1f85c7ebb4ee0e6045eb0e5db987a76209838f69f`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065a8420959a3c31f08f22599784d93334ea42cfe102e8096372ce3535b744ca`  
		Last Modified: Mon, 06 Jun 2022 23:56:42 GMT  
		Size: 113.7 MB (113727928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218765ecdc92ddbb127c4fa8d00d71deeb947040f31ef34ddec95ea7cbe23676`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:32ac0f06eb8208c29dcd8f48b6b5120f4a09c7d1986eea12c160e49f1f304d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224152225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a8d50a9b72b5d372fa2d247359ea8c16eeb9a96422b4c8639ebcd07516e652`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:36:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 04:38:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 04:38:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 04:38:37 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 04:38:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 04:38:41 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 04:38:42 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 04:38:43 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 04:38:44 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 04:38:45 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 04:38:46 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 07 Jun 2022 04:38:47 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 07 Jun 2022 04:38:48 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 07 Jun 2022 04:38:49 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 04:38:50 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 04:38:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 04:38:52 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 04:38:54 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 07 Jun 2022 04:39:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 07 Jun 2022 04:39:03 GMT
ENV HTTP_API=false
# Tue, 07 Jun 2022 04:39:04 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 04:39:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 04:39:06 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 04:39:07 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90c2e8ebba1a8c8c808dc0fc6713296767a6225346074a494da934e5eb1bffe`  
		Last Modified: Tue, 07 Jun 2022 04:40:58 GMT  
		Size: 85.8 MB (85823076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f858118dd99d6115eb2738eae4edbabda7fcd72b175c8bbb4f39e84e990b38f`  
		Last Modified: Tue, 07 Jun 2022 04:40:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cdd70aa503c2012f6c338f499d198c1fb27d4877f434e6b236fe78ea2f603c`  
		Last Modified: Tue, 07 Jun 2022 04:40:46 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d206c9b11ef37af5da73286104d4d2fdc9c84521778888387ddeb57ff9e1452a`  
		Last Modified: Tue, 07 Jun 2022 04:40:45 GMT  
		Size: 859.5 KB (859531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a211292cefd1b6fa526ab765b315d54614b40a4c920cc6bd223dab23fbb99fc`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf469e907a3e246b0344a753c7c4e926f314e4ee5f49009d76b06cee65b0f93`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d9c7e13abd4a2911c642e9eb0b206f5d366c496d20c9b7db27f11e69b1ab3a`  
		Last Modified: Tue, 07 Jun 2022 04:40:54 GMT  
		Size: 113.7 MB (113727876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3009fa1d28a134141a124574334d55f7cd7c043cab361fd58e9e35ef6439eeb`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.2-u0` - linux; ppc64le

```console
$ docker pull bonita@sha256:b60dcfbbd19ee916cfe82496a0a3ec32704fb02d7ef614a462a8c26b419f33ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231616671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5c514531c3d593534bda4827d79ab938f9b69604af9911b69e50720c9c5a6c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:06:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 10:14:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:14:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 10:14:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 10:14:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 10:14:35 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 10:14:37 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 10:14:42 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 10:14:44 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 10:14:46 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 10:14:50 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 07 Jun 2022 10:14:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 07 Jun 2022 10:14:57 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 07 Jun 2022 10:15:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 10:15:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 10:15:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 10:15:14 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 10:15:15 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 07 Jun 2022 10:15:32 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 07 Jun 2022 10:15:36 GMT
ENV HTTP_API=false
# Tue, 07 Jun 2022 10:15:42 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 10:15:45 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 10:15:51 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 10:15:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a331e660ead68d382742f61a8656c41551cb44956552a658c4a7b744bface060`  
		Last Modified: Tue, 07 Jun 2022 10:17:56 GMT  
		Size: 86.6 MB (86607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213b14ccc59baf8fae328306aad1c663e545d1071ae41070ca2f4b8407c3ce1`  
		Last Modified: Tue, 07 Jun 2022 10:17:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849223db8c9360d39904a129a16fcab82cc75ed0440f6b216c84181e8eaf3a9d`  
		Last Modified: Tue, 07 Jun 2022 10:17:41 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cbc038830160e8447b4c94a591d38b99d4212b0cf63674dc8d0512708ccc57`  
		Last Modified: Tue, 07 Jun 2022 10:17:39 GMT  
		Size: 831.6 KB (831568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b68ec78a742cf1aa2513ae7a692d0fe38f63e39b8360ae6358423caa08434`  
		Last Modified: Tue, 07 Jun 2022 10:17:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa847ac20a1fea971cba2a4054299001b79527c44c7aee950a97916aa8a7bfb`  
		Last Modified: Tue, 07 Jun 2022 10:17:38 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a42bd5762b185dffd9c65896d1caace35c218bc37c33dc07dd6f212844fbcb1`  
		Last Modified: Tue, 07 Jun 2022 10:17:49 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b94e67f1cc5eec539069c00057c5a4de04b37c4fd1b7077caca27601fc9b130`  
		Last Modified: Tue, 07 Jun 2022 10:17:38 GMT  
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
$ docker pull bonita@sha256:c182a52b08288f0cd5a0d26d53676fc2de24028566afa05342c0daac600ee5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:92e624d5d12bd76f28df3d738c9273a9574052ad2e3ad43b1630fff17bca9e3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234278497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571852e575101716d705aec04320ad4fc0dff615ceb71e8a15a7596b766be76`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:53:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 06 Jun 2022 23:54:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 23:54:17 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 06 Jun 2022 23:54:17 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 06 Jun 2022 23:54:20 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BONITA_VERSION
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BONITA_SHA256
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BASE_URL
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BONITA_URL
# Mon, 06 Jun 2022 23:54:21 GMT
ENV BONITA_VERSION=7.11.4
# Mon, 06 Jun 2022 23:54:21 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Mon, 06 Jun 2022 23:54:21 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Mon, 06 Jun 2022 23:54:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 06 Jun 2022 23:54:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Mon, 06 Jun 2022 23:54:22 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 06 Jun 2022 23:54:22 GMT
RUN mkdir /opt/files
# Mon, 06 Jun 2022 23:54:22 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Mon, 06 Jun 2022 23:54:29 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Mon, 06 Jun 2022 23:54:30 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 06 Jun 2022 23:54:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 06 Jun 2022 23:54:32 GMT
VOLUME [/opt/bonita]
# Mon, 06 Jun 2022 23:54:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 06 Jun 2022 23:54:32 GMT
EXPOSE 8080
# Mon, 06 Jun 2022 23:54:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5418a805118d48622924b6aafd90b6d0fd41a00a2afcb8573edae873ad6b34`  
		Last Modified: Mon, 06 Jun 2022 23:56:08 GMT  
		Size: 93.7 MB (93701902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebb439837c2100d990d18cf836fa05055e32fd2bdd47a14fafc56564be51aa`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7653bdf398cf2fea20e659373f67f4403ad79ba2bc386834784dcf81a6f22b`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed9d5128126c39997f43cfed11e39f999bb3e5dc68cc31cce7ec17a24c9f99`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dd2aa7edc06423ff835a63a9ae711c72338cb3ef1e5b71f7f701f916a5cc2a`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3a45046859f9644074c64249c4d2fb2cf67aeacc7747d76e97a18e0a64c4c1`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac198f917e6544accba41fd47067edf2e82af10bc8bc63a49f8f3cdf26026b0`  
		Last Modified: Mon, 06 Jun 2022 23:55:59 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15689045d0a7e0550fed3bfab21a8fb36b1a6ab15b43089a9dcd7383c504c481`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c7a210928461ca9ab03db2c0acbe00176bb3917c5b7df5f9081bc34725bb90fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223391964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d855f8e9fa66615e529bc05badaca2919af95addc94a642f728bd9f9bac22513`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:36:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 04:36:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 04:37:00 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 04:37:01 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 04:37:05 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 04:37:06 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 04:37:07 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 04:37:08 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 04:37:09 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 04:37:10 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 07 Jun 2022 04:37:11 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 07 Jun 2022 04:37:12 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 07 Jun 2022 04:37:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 04:37:14 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 07 Jun 2022 04:37:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 04:37:16 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 04:37:18 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 07 Jun 2022 04:37:25 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 07 Jun 2022 04:37:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 04:37:28 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 04:37:28 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 04:37:30 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 04:37:30 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 04:37:31 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38187bb0cb1b93156315bff2294d1f517eee8c1d07300ab33d2453b96dce44b8`  
		Last Modified: Tue, 07 Jun 2022 04:40:03 GMT  
		Size: 85.8 MB (85823061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f02956b16c6742ce9547c2690d9faf5a1ba2b8b0638890a467c728ed26262c3`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5c77638ac3681fd4230f8794542276a7d5ed539a3696f7766ac5eed4290cec`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de196c1ba37cbc23fccaf116fef01edf217eb86d5ccd722c8669491021200dc`  
		Last Modified: Tue, 07 Jun 2022 04:39:49 GMT  
		Size: 475.8 KB (475763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9103860839dea273b7a392c9e538eca98a49bf649a4d4a79b077dc6addc717a`  
		Last Modified: Tue, 07 Jun 2022 04:39:49 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531ee8d9ac8984e5cc1e3e257fca75b651f3c3d1d19bfc8fa629ca92feb34cca`  
		Last Modified: Tue, 07 Jun 2022 04:39:48 GMT  
		Size: 6.9 KB (6868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef63d3b1e2d13e9ddc13e9304930f3b86bf3aa1c9fa944af0ad5d919787bef6`  
		Last Modified: Tue, 07 Jun 2022 04:40:00 GMT  
		Size: 113.3 MB (113347831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9415e34f133705c11e15c326f0f8c7d43d28020d64e79ef06b8afd38b8801a6d`  
		Last Modified: Tue, 07 Jun 2022 04:39:48 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:42015c88f159169c44924f419d339b2b7808e0de3efda20d6b518f7abd57b64a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230883546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1beed798a8424e06ab63bfa05049f88aa24104bad94ab900a6a86c5487b29f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:06:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 10:08:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:08:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 10:08:26 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 10:08:38 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 10:08:42 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 10:08:44 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 10:08:50 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 10:08:53 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 10:08:59 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 07 Jun 2022 10:09:02 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 07 Jun 2022 10:09:05 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 07 Jun 2022 10:09:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 10:09:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 07 Jun 2022 10:09:18 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 10:09:24 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 10:09:27 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 07 Jun 2022 10:09:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 07 Jun 2022 10:09:49 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 10:09:56 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 10:09:59 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 10:10:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 10:10:03 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 10:10:08 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5932cab289b2b2a387d18cfb709811f1a652f05e78ced57c596e0e3a7136ca8f`  
		Last Modified: Tue, 07 Jun 2022 10:16:56 GMT  
		Size: 86.6 MB (86606720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e99318a085a88c3b7eefb71e0fb1851bbc6f00b8b9b350cd5f611e0e3294356`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128478c35447ca89ff14fbf5c1a1a2936a18e0012a7f08f2db12e421b6d46159`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4873185aa919a50c4fad4b47828805af6df63bc92c8143b5268a777fade09b6`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 475.3 KB (475347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc9dd2be22b30ab96107306d3decb7df1bdafed73b547ca9f50c89681528132`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acd8f5bfe97b576b0d76542fe23769024f6342f29204f006a93e252577d91ff`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555aab78bd51927009b5cff45506381876e0d93e3f958331eb0bf1aafe16b35f`  
		Last Modified: Tue, 07 Jun 2022 10:16:47 GMT  
		Size: 113.3 MB (113347827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bf4efa22c46743f8d6a52f1c7f11ff4c18a9682323e302959e76679447be74`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:c182a52b08288f0cd5a0d26d53676fc2de24028566afa05342c0daac600ee5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:92e624d5d12bd76f28df3d738c9273a9574052ad2e3ad43b1630fff17bca9e3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.3 MB (234278497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571852e575101716d705aec04320ad4fc0dff615ceb71e8a15a7596b766be76`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:53:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 06 Jun 2022 23:54:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 23:54:17 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 06 Jun 2022 23:54:17 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 06 Jun 2022 23:54:20 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BONITA_VERSION
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BONITA_SHA256
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BASE_URL
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BONITA_URL
# Mon, 06 Jun 2022 23:54:21 GMT
ENV BONITA_VERSION=7.11.4
# Mon, 06 Jun 2022 23:54:21 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Mon, 06 Jun 2022 23:54:21 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Mon, 06 Jun 2022 23:54:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 06 Jun 2022 23:54:21 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Mon, 06 Jun 2022 23:54:22 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 06 Jun 2022 23:54:22 GMT
RUN mkdir /opt/files
# Mon, 06 Jun 2022 23:54:22 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Mon, 06 Jun 2022 23:54:29 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Mon, 06 Jun 2022 23:54:30 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 06 Jun 2022 23:54:31 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 06 Jun 2022 23:54:32 GMT
VOLUME [/opt/bonita]
# Mon, 06 Jun 2022 23:54:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 06 Jun 2022 23:54:32 GMT
EXPOSE 8080
# Mon, 06 Jun 2022 23:54:32 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5418a805118d48622924b6aafd90b6d0fd41a00a2afcb8573edae873ad6b34`  
		Last Modified: Mon, 06 Jun 2022 23:56:08 GMT  
		Size: 93.7 MB (93701902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebb439837c2100d990d18cf836fa05055e32fd2bdd47a14fafc56564be51aa`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7653bdf398cf2fea20e659373f67f4403ad79ba2bc386834784dcf81a6f22b`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed9d5128126c39997f43cfed11e39f999bb3e5dc68cc31cce7ec17a24c9f99`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dd2aa7edc06423ff835a63a9ae711c72338cb3ef1e5b71f7f701f916a5cc2a`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3a45046859f9644074c64249c4d2fb2cf67aeacc7747d76e97a18e0a64c4c1`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 6.9 KB (6892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ac198f917e6544accba41fd47067edf2e82af10bc8bc63a49f8f3cdf26026b0`  
		Last Modified: Mon, 06 Jun 2022 23:55:59 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15689045d0a7e0550fed3bfab21a8fb36b1a6ab15b43089a9dcd7383c504c481`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c7a210928461ca9ab03db2c0acbe00176bb3917c5b7df5f9081bc34725bb90fe
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223391964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d855f8e9fa66615e529bc05badaca2919af95addc94a642f728bd9f9bac22513`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:36:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 04:36:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 04:37:00 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 04:37:01 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 04:37:05 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 04:37:06 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 04:37:07 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 04:37:08 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 04:37:09 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 04:37:10 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 07 Jun 2022 04:37:11 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 07 Jun 2022 04:37:12 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 07 Jun 2022 04:37:13 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 04:37:14 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 07 Jun 2022 04:37:15 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 04:37:16 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 04:37:18 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 07 Jun 2022 04:37:25 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 07 Jun 2022 04:37:26 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 04:37:28 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 04:37:28 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 04:37:30 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 04:37:30 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 04:37:31 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38187bb0cb1b93156315bff2294d1f517eee8c1d07300ab33d2453b96dce44b8`  
		Last Modified: Tue, 07 Jun 2022 04:40:03 GMT  
		Size: 85.8 MB (85823061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f02956b16c6742ce9547c2690d9faf5a1ba2b8b0638890a467c728ed26262c3`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5c77638ac3681fd4230f8794542276a7d5ed539a3696f7766ac5eed4290cec`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de196c1ba37cbc23fccaf116fef01edf217eb86d5ccd722c8669491021200dc`  
		Last Modified: Tue, 07 Jun 2022 04:39:49 GMT  
		Size: 475.8 KB (475763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9103860839dea273b7a392c9e538eca98a49bf649a4d4a79b077dc6addc717a`  
		Last Modified: Tue, 07 Jun 2022 04:39:49 GMT  
		Size: 113.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531ee8d9ac8984e5cc1e3e257fca75b651f3c3d1d19bfc8fa629ca92feb34cca`  
		Last Modified: Tue, 07 Jun 2022 04:39:48 GMT  
		Size: 6.9 KB (6868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ef63d3b1e2d13e9ddc13e9304930f3b86bf3aa1c9fa944af0ad5d919787bef6`  
		Last Modified: Tue, 07 Jun 2022 04:40:00 GMT  
		Size: 113.3 MB (113347831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9415e34f133705c11e15c326f0f8c7d43d28020d64e79ef06b8afd38b8801a6d`  
		Last Modified: Tue, 07 Jun 2022 04:39:48 GMT  
		Size: 1.7 KB (1685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:42015c88f159169c44924f419d339b2b7808e0de3efda20d6b518f7abd57b64a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230883546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb1beed798a8424e06ab63bfa05049f88aa24104bad94ab900a6a86c5487b29f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:06:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 10:08:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:08:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 10:08:26 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 10:08:38 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 10:08:42 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 10:08:44 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 10:08:50 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 10:08:53 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 10:08:59 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 07 Jun 2022 10:09:02 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 07 Jun 2022 10:09:05 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 07 Jun 2022 10:09:08 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 10:09:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 07 Jun 2022 10:09:18 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 10:09:24 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 10:09:27 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 07 Jun 2022 10:09:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 07 Jun 2022 10:09:49 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 10:09:56 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 10:09:59 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 10:10:00 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 10:10:03 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 10:10:08 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5932cab289b2b2a387d18cfb709811f1a652f05e78ced57c596e0e3a7136ca8f`  
		Last Modified: Tue, 07 Jun 2022 10:16:56 GMT  
		Size: 86.6 MB (86606720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e99318a085a88c3b7eefb71e0fb1851bbc6f00b8b9b350cd5f611e0e3294356`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128478c35447ca89ff14fbf5c1a1a2936a18e0012a7f08f2db12e421b6d46159`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4873185aa919a50c4fad4b47828805af6df63bc92c8143b5268a777fade09b6`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 475.3 KB (475347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc9dd2be22b30ab96107306d3decb7df1bdafed73b547ca9f50c89681528132`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acd8f5bfe97b576b0d76542fe23769024f6342f29204f006a93e252577d91ff`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 6.9 KB (6896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555aab78bd51927009b5cff45506381876e0d93e3f958331eb0bf1aafe16b35f`  
		Last Modified: Tue, 07 Jun 2022 10:16:47 GMT  
		Size: 113.3 MB (113347827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48bf4efa22c46743f8d6a52f1c7f11ff4c18a9682323e302959e76679447be74`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:7c4f89e1a1c71329633982be8af74bdaec5fd465bebd1cfc3ca3d9996c07293b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:b3d60108d31746ac6b0a250ae5a1584f9c5feb1dbde7a14b7be51ee2d25c9677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237346125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f5d5bedf104280789d1778c459816bba7d492f11c51cd0c75785c2ca77d3dc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:53:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 06 Jun 2022 23:54:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 23:54:17 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 06 Jun 2022 23:54:17 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 06 Jun 2022 23:54:20 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BONITA_VERSION
# Mon, 06 Jun 2022 23:54:39 GMT
ARG BRANDING_VERSION
# Mon, 06 Jun 2022 23:54:39 GMT
ARG BONITA_SHA256
# Mon, 06 Jun 2022 23:54:39 GMT
ARG BASE_URL
# Mon, 06 Jun 2022 23:54:40 GMT
ARG BONITA_URL
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 06 Jun 2022 23:54:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 06 Jun 2022 23:54:41 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 06 Jun 2022 23:54:41 GMT
RUN mkdir /opt/files
# Mon, 06 Jun 2022 23:54:41 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 06 Jun 2022 23:54:50 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 06 Jun 2022 23:54:52 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 06 Jun 2022 23:54:53 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 06 Jun 2022 23:54:53 GMT
VOLUME [/opt/bonita]
# Mon, 06 Jun 2022 23:54:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 06 Jun 2022 23:54:53 GMT
EXPOSE 8080
# Mon, 06 Jun 2022 23:54:53 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5418a805118d48622924b6aafd90b6d0fd41a00a2afcb8573edae873ad6b34`  
		Last Modified: Mon, 06 Jun 2022 23:56:08 GMT  
		Size: 93.7 MB (93701902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebb439837c2100d990d18cf836fa05055e32fd2bdd47a14fafc56564be51aa`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7653bdf398cf2fea20e659373f67f4403ad79ba2bc386834784dcf81a6f22b`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed9d5128126c39997f43cfed11e39f999bb3e5dc68cc31cce7ec17a24c9f99`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5561b5cdb8e81171f8ee8e8cf79d43e8ca90f682045252d97da3e8b342da0c`  
		Last Modified: Mon, 06 Jun 2022 23:56:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b1e69431891ab97af4b6be65a109d9dd07fed3c1d3e1c9feff6e32e84d408e`  
		Last Modified: Mon, 06 Jun 2022 23:56:18 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419207b701157759dda6e80cb1d11230516c456e02a170a509e6a2f807a2e41`  
		Last Modified: Mon, 06 Jun 2022 23:56:23 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d0fd575eecb3ac1fd07bf640b251c18acba86b6dbbe620f052072e37845462`  
		Last Modified: Mon, 06 Jun 2022 23:56:18 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c146fc722b92c15bb4d66f80cd54795c1097312882641b94b14c0d39cd735d71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226459583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a34adb98477ca9f8e45e840592d9d5df5bf8491e4adf0b2e471ec80372035e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:36:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 04:36:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 04:37:00 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 04:37:01 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 04:37:05 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 04:37:06 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 04:37:36 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 04:37:37 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 04:37:38 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 04:37:39 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 04:37:40 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 07 Jun 2022 04:37:41 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 07 Jun 2022 04:37:42 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 07 Jun 2022 04:37:43 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 04:37:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 04:37:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 04:37:46 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 04:37:47 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 04:37:49 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 07 Jun 2022 04:37:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 07 Jun 2022 04:38:00 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 04:38:02 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 04:38:02 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 04:38:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 04:38:04 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 04:38:05 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38187bb0cb1b93156315bff2294d1f517eee8c1d07300ab33d2453b96dce44b8`  
		Last Modified: Tue, 07 Jun 2022 04:40:03 GMT  
		Size: 85.8 MB (85823061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f02956b16c6742ce9547c2690d9faf5a1ba2b8b0638890a467c728ed26262c3`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5c77638ac3681fd4230f8794542276a7d5ed539a3696f7766ac5eed4290cec`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de196c1ba37cbc23fccaf116fef01edf217eb86d5ccd722c8669491021200dc`  
		Last Modified: Tue, 07 Jun 2022 04:39:49 GMT  
		Size: 475.8 KB (475763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed2fbaa18fc80b7a55fab9e966653d48bb94b52f47cfd33563b15aee52acfbb`  
		Last Modified: Tue, 07 Jun 2022 04:40:15 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92060965857675ec3f90ee8d339a56e4494c0c5f2fc1e7204e923ffa9a01582`  
		Last Modified: Tue, 07 Jun 2022 04:40:15 GMT  
		Size: 6.9 KB (6917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e974e1fc9a3b22f57f88118b5ab8c9031fcdcb9b6ba8f2a082eb8b1268f669bd`  
		Last Modified: Tue, 07 Jun 2022 04:40:28 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f617b62b56fdf2ca59df149c7258fc5dfe4cd6b78244eda3418f811c5ab13`  
		Last Modified: Tue, 07 Jun 2022 04:40:15 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:b56b3ae5fd5e336c93594767ecae7a32026f87bf5ffd09a13f55c8d45123f978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233951178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9fec1db19fcffd6ebef6c9cae4f880271ccbbfa9600fc7146eeb41f40158d6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:06:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 10:08:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:08:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 10:08:26 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 10:08:38 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 10:08:42 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 10:10:29 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 10:10:30 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 10:10:32 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 10:10:35 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 10:10:38 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 07 Jun 2022 10:10:41 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 07 Jun 2022 10:10:44 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 07 Jun 2022 10:10:46 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 10:10:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 10:10:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 10:10:55 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 10:11:01 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 10:11:02 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 07 Jun 2022 10:11:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 07 Jun 2022 10:11:19 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 10:11:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 10:11:30 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 10:11:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 10:11:33 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 10:11:36 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5932cab289b2b2a387d18cfb709811f1a652f05e78ced57c596e0e3a7136ca8f`  
		Last Modified: Tue, 07 Jun 2022 10:16:56 GMT  
		Size: 86.6 MB (86606720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e99318a085a88c3b7eefb71e0fb1851bbc6f00b8b9b350cd5f611e0e3294356`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128478c35447ca89ff14fbf5c1a1a2936a18e0012a7f08f2db12e421b6d46159`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4873185aa919a50c4fad4b47828805af6df63bc92c8143b5268a777fade09b6`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 475.3 KB (475347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eceaedc2b9083c2b4baf061ec3fad71b09f51e83d5e7ae2b07aa70e01bc60d3`  
		Last Modified: Tue, 07 Jun 2022 10:17:09 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba561c4766c632072d54ee899d6956320cc379ead197e70321d06a5936402f0c`  
		Last Modified: Tue, 07 Jun 2022 10:17:09 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b5afedaeef8dad41a823655dbe702900e9f84fbb2f98bbf9f560534a33c0c9`  
		Last Modified: Tue, 07 Jun 2022 10:17:22 GMT  
		Size: 116.4 MB (116415403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56f59b30a77def4359279676b77dc14e03c625eb67a39ae191af44d2125d0f`  
		Last Modified: Tue, 07 Jun 2022 10:17:09 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:7c4f89e1a1c71329633982be8af74bdaec5fd465bebd1cfc3ca3d9996c07293b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:b3d60108d31746ac6b0a250ae5a1584f9c5feb1dbde7a14b7be51ee2d25c9677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.3 MB (237346125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f5d5bedf104280789d1778c459816bba7d492f11c51cd0c75785c2ca77d3dc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:53:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 06 Jun 2022 23:54:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 23:54:17 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 06 Jun 2022 23:54:17 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 06 Jun 2022 23:54:20 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 06 Jun 2022 23:54:20 GMT
ARG BONITA_VERSION
# Mon, 06 Jun 2022 23:54:39 GMT
ARG BRANDING_VERSION
# Mon, 06 Jun 2022 23:54:39 GMT
ARG BONITA_SHA256
# Mon, 06 Jun 2022 23:54:39 GMT
ARG BASE_URL
# Mon, 06 Jun 2022 23:54:40 GMT
ARG BONITA_URL
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BONITA_VERSION=7.12.1
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BRANDING_VERSION=2021.1
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Mon, 06 Jun 2022 23:54:40 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 06 Jun 2022 23:54:40 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Mon, 06 Jun 2022 23:54:41 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Mon, 06 Jun 2022 23:54:41 GMT
RUN mkdir /opt/files
# Mon, 06 Jun 2022 23:54:41 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Mon, 06 Jun 2022 23:54:50 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Mon, 06 Jun 2022 23:54:52 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Mon, 06 Jun 2022 23:54:53 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Mon, 06 Jun 2022 23:54:53 GMT
VOLUME [/opt/bonita]
# Mon, 06 Jun 2022 23:54:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 06 Jun 2022 23:54:53 GMT
EXPOSE 8080
# Mon, 06 Jun 2022 23:54:53 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5418a805118d48622924b6aafd90b6d0fd41a00a2afcb8573edae873ad6b34`  
		Last Modified: Mon, 06 Jun 2022 23:56:08 GMT  
		Size: 93.7 MB (93701902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ebb439837c2100d990d18cf836fa05055e32fd2bdd47a14fafc56564be51aa`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab7653bdf398cf2fea20e659373f67f4403ad79ba2bc386834784dcf81a6f22b`  
		Last Modified: Mon, 06 Jun 2022 23:55:56 GMT  
		Size: 1.9 KB (1885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ed9d5128126c39997f43cfed11e39f999bb3e5dc68cc31cce7ec17a24c9f99`  
		Last Modified: Mon, 06 Jun 2022 23:55:54 GMT  
		Size: 506.4 KB (506350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f5561b5cdb8e81171f8ee8e8cf79d43e8ca90f682045252d97da3e8b342da0c`  
		Last Modified: Mon, 06 Jun 2022 23:56:18 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b1e69431891ab97af4b6be65a109d9dd07fed3c1d3e1c9feff6e32e84d408e`  
		Last Modified: Mon, 06 Jun 2022 23:56:18 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9419207b701157759dda6e80cb1d11230516c456e02a170a509e6a2f807a2e41`  
		Last Modified: Mon, 06 Jun 2022 23:56:23 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d0fd575eecb3ac1fd07bf640b251c18acba86b6dbbe620f052072e37845462`  
		Last Modified: Mon, 06 Jun 2022 23:56:18 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:c146fc722b92c15bb4d66f80cd54795c1097312882641b94b14c0d39cd735d71
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.5 MB (226459583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a34adb98477ca9f8e45e840592d9d5df5bf8491e4adf0b2e471ec80372035e`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:36:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 04:36:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 04:37:00 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 04:37:01 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 04:37:05 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 04:37:06 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 04:37:36 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 04:37:37 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 04:37:38 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 04:37:39 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 04:37:40 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 07 Jun 2022 04:37:41 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 07 Jun 2022 04:37:42 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 07 Jun 2022 04:37:43 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 04:37:44 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 04:37:45 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 04:37:46 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 04:37:47 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 04:37:49 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 07 Jun 2022 04:37:59 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 07 Jun 2022 04:38:00 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 04:38:02 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 04:38:02 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 04:38:04 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 04:38:04 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 04:38:05 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38187bb0cb1b93156315bff2294d1f517eee8c1d07300ab33d2453b96dce44b8`  
		Last Modified: Tue, 07 Jun 2022 04:40:03 GMT  
		Size: 85.8 MB (85823061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f02956b16c6742ce9547c2690d9faf5a1ba2b8b0638890a467c728ed26262c3`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5c77638ac3681fd4230f8794542276a7d5ed539a3696f7766ac5eed4290cec`  
		Last Modified: Tue, 07 Jun 2022 04:39:51 GMT  
		Size: 1.9 KB (1857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de196c1ba37cbc23fccaf116fef01edf217eb86d5ccd722c8669491021200dc`  
		Last Modified: Tue, 07 Jun 2022 04:39:49 GMT  
		Size: 475.8 KB (475763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ed2fbaa18fc80b7a55fab9e966653d48bb94b52f47cfd33563b15aee52acfbb`  
		Last Modified: Tue, 07 Jun 2022 04:40:15 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92060965857675ec3f90ee8d339a56e4494c0c5f2fc1e7204e923ffa9a01582`  
		Last Modified: Tue, 07 Jun 2022 04:40:15 GMT  
		Size: 6.9 KB (6917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e974e1fc9a3b22f57f88118b5ab8c9031fcdcb9b6ba8f2a082eb8b1268f669bd`  
		Last Modified: Tue, 07 Jun 2022 04:40:28 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04f617b62b56fdf2ca59df149c7258fc5dfe4cd6b78244eda3418f811c5ab13`  
		Last Modified: Tue, 07 Jun 2022 04:40:15 GMT  
		Size: 1.7 KB (1683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:b56b3ae5fd5e336c93594767ecae7a32026f87bf5ffd09a13f55c8d45123f978
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.0 MB (233951178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9fec1db19fcffd6ebef6c9cae4f880271ccbbfa9600fc7146eeb41f40158d6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:06:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 10:08:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:08:18 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 10:08:26 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 10:08:38 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 10:08:42 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 10:10:29 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 10:10:30 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 10:10:32 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 10:10:35 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 10:10:38 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 07 Jun 2022 10:10:41 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 07 Jun 2022 10:10:44 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 07 Jun 2022 10:10:46 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 10:10:48 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 10:10:49 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 07 Jun 2022 10:10:55 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 07 Jun 2022 10:11:01 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 10:11:02 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 07 Jun 2022 10:11:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 07 Jun 2022 10:11:19 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 07 Jun 2022 10:11:26 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 07 Jun 2022 10:11:30 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 10:11:31 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 10:11:33 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 10:11:36 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5932cab289b2b2a387d18cfb709811f1a652f05e78ced57c596e0e3a7136ca8f`  
		Last Modified: Tue, 07 Jun 2022 10:16:56 GMT  
		Size: 86.6 MB (86606720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e99318a085a88c3b7eefb71e0fb1851bbc6f00b8b9b350cd5f611e0e3294356`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:128478c35447ca89ff14fbf5c1a1a2936a18e0012a7f08f2db12e421b6d46159`  
		Last Modified: Tue, 07 Jun 2022 10:16:42 GMT  
		Size: 1.9 KB (1884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4873185aa919a50c4fad4b47828805af6df63bc92c8143b5268a777fade09b6`  
		Last Modified: Tue, 07 Jun 2022 10:16:39 GMT  
		Size: 475.3 KB (475347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eceaedc2b9083c2b4baf061ec3fad71b09f51e83d5e7ae2b07aa70e01bc60d3`  
		Last Modified: Tue, 07 Jun 2022 10:17:09 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba561c4766c632072d54ee899d6956320cc379ead197e70321d06a5936402f0c`  
		Last Modified: Tue, 07 Jun 2022 10:17:09 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b5afedaeef8dad41a823655dbe702900e9f84fbb2f98bbf9f560534a33c0c9`  
		Last Modified: Tue, 07 Jun 2022 10:17:22 GMT  
		Size: 116.4 MB (116415403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf56f59b30a77def4359279676b77dc14e03c625eb67a39ae191af44d2125d0f`  
		Last Modified: Tue, 07 Jun 2022 10:17:09 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13`

```console
$ docker pull bonita@sha256:cb21f182992224f7d03dba6e5ee6a579d411f48a18fb16f40c492487b5fa4b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13` - linux; amd64

```console
$ docker pull bonita@sha256:ee74276139bf7c8a87f356b14edb98fa6bad507ff9a372aa1c605cada4649f3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235082013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ac44f6589b4a64d0ed54d539632fd9198c6e5d28d636d341ede8cf4325d306`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:53:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 06 Jun 2022 23:55:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 23:55:18 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 06 Jun 2022 23:55:18 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 06 Jun 2022 23:55:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BONITA_VERSION
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BRANDING_VERSION
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BONITA_SHA256
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BASE_URL
# Mon, 06 Jun 2022 23:55:22 GMT
ARG BONITA_URL
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_VERSION=7.13.0
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BRANDING_VERSION=2021.2-u0
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Mon, 06 Jun 2022 23:55:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Mon, 06 Jun 2022 23:55:23 GMT
RUN mkdir /opt/files
# Mon, 06 Jun 2022 23:55:23 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Mon, 06 Jun 2022 23:55:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Mon, 06 Jun 2022 23:55:32 GMT
ENV HTTP_API=false
# Mon, 06 Jun 2022 23:55:32 GMT
VOLUME [/opt/bonita]
# Mon, 06 Jun 2022 23:55:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 06 Jun 2022 23:55:33 GMT
EXPOSE 8080
# Mon, 06 Jun 2022 23:55:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1e67ee570f875ac56d020bb9ba2048a4b6afe001f2abf27cfcddb94522850b`  
		Last Modified: Mon, 06 Jun 2022 23:56:51 GMT  
		Size: 93.7 MB (93704786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c799895347844414e50219a00d72f2823de2835c43da6467690a7dfd8092c060`  
		Last Modified: Mon, 06 Jun 2022 23:56:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c498ca5f2196c619a41699208691a92297201323322f46a997527f30a6f4b`  
		Last Modified: Mon, 06 Jun 2022 23:56:38 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2f7a93399ccd26ef9ccf374b0aa06222a048a869aafe199d501d1502d94dd5`  
		Last Modified: Mon, 06 Jun 2022 23:56:37 GMT  
		Size: 930.5 KB (930477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e210e87ebbe93c80e1d898c2ed2ebdc54aca26d7a6a717cf3aa099924d61d90`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae012376ae09d981dd1cd1f1f85c7ebb4ee0e6045eb0e5db987a76209838f69f`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065a8420959a3c31f08f22599784d93334ea42cfe102e8096372ce3535b744ca`  
		Last Modified: Mon, 06 Jun 2022 23:56:42 GMT  
		Size: 113.7 MB (113727928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218765ecdc92ddbb127c4fa8d00d71deeb947040f31ef34ddec95ea7cbe23676`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:32ac0f06eb8208c29dcd8f48b6b5120f4a09c7d1986eea12c160e49f1f304d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224152225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a8d50a9b72b5d372fa2d247359ea8c16eeb9a96422b4c8639ebcd07516e652`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:36:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 04:38:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 04:38:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 04:38:37 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 04:38:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 04:38:41 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 04:38:42 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 04:38:43 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 04:38:44 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 04:38:45 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 04:38:46 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 07 Jun 2022 04:38:47 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 07 Jun 2022 04:38:48 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 07 Jun 2022 04:38:49 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 04:38:50 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 04:38:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 04:38:52 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 04:38:54 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 07 Jun 2022 04:39:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 07 Jun 2022 04:39:03 GMT
ENV HTTP_API=false
# Tue, 07 Jun 2022 04:39:04 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 04:39:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 04:39:06 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 04:39:07 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90c2e8ebba1a8c8c808dc0fc6713296767a6225346074a494da934e5eb1bffe`  
		Last Modified: Tue, 07 Jun 2022 04:40:58 GMT  
		Size: 85.8 MB (85823076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f858118dd99d6115eb2738eae4edbabda7fcd72b175c8bbb4f39e84e990b38f`  
		Last Modified: Tue, 07 Jun 2022 04:40:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cdd70aa503c2012f6c338f499d198c1fb27d4877f434e6b236fe78ea2f603c`  
		Last Modified: Tue, 07 Jun 2022 04:40:46 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d206c9b11ef37af5da73286104d4d2fdc9c84521778888387ddeb57ff9e1452a`  
		Last Modified: Tue, 07 Jun 2022 04:40:45 GMT  
		Size: 859.5 KB (859531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a211292cefd1b6fa526ab765b315d54614b40a4c920cc6bd223dab23fbb99fc`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf469e907a3e246b0344a753c7c4e926f314e4ee5f49009d76b06cee65b0f93`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d9c7e13abd4a2911c642e9eb0b206f5d366c496d20c9b7db27f11e69b1ab3a`  
		Last Modified: Tue, 07 Jun 2022 04:40:54 GMT  
		Size: 113.7 MB (113727876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3009fa1d28a134141a124574334d55f7cd7c043cab361fd58e9e35ef6439eeb`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13` - linux; ppc64le

```console
$ docker pull bonita@sha256:b60dcfbbd19ee916cfe82496a0a3ec32704fb02d7ef614a462a8c26b419f33ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231616671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5c514531c3d593534bda4827d79ab938f9b69604af9911b69e50720c9c5a6c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:06:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 10:14:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:14:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 10:14:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 10:14:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 10:14:35 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 10:14:37 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 10:14:42 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 10:14:44 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 10:14:46 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 10:14:50 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 07 Jun 2022 10:14:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 07 Jun 2022 10:14:57 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 07 Jun 2022 10:15:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 10:15:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 10:15:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 10:15:14 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 10:15:15 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 07 Jun 2022 10:15:32 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 07 Jun 2022 10:15:36 GMT
ENV HTTP_API=false
# Tue, 07 Jun 2022 10:15:42 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 10:15:45 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 10:15:51 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 10:15:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a331e660ead68d382742f61a8656c41551cb44956552a658c4a7b744bface060`  
		Last Modified: Tue, 07 Jun 2022 10:17:56 GMT  
		Size: 86.6 MB (86607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213b14ccc59baf8fae328306aad1c663e545d1071ae41070ca2f4b8407c3ce1`  
		Last Modified: Tue, 07 Jun 2022 10:17:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849223db8c9360d39904a129a16fcab82cc75ed0440f6b216c84181e8eaf3a9d`  
		Last Modified: Tue, 07 Jun 2022 10:17:41 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cbc038830160e8447b4c94a591d38b99d4212b0cf63674dc8d0512708ccc57`  
		Last Modified: Tue, 07 Jun 2022 10:17:39 GMT  
		Size: 831.6 KB (831568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b68ec78a742cf1aa2513ae7a692d0fe38f63e39b8360ae6358423caa08434`  
		Last Modified: Tue, 07 Jun 2022 10:17:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa847ac20a1fea971cba2a4054299001b79527c44c7aee950a97916aa8a7bfb`  
		Last Modified: Tue, 07 Jun 2022 10:17:38 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a42bd5762b185dffd9c65896d1caace35c218bc37c33dc07dd6f212844fbcb1`  
		Last Modified: Tue, 07 Jun 2022 10:17:49 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b94e67f1cc5eec539069c00057c5a4de04b37c4fd1b7077caca27601fc9b130`  
		Last Modified: Tue, 07 Jun 2022 10:17:38 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.13.0`

```console
$ docker pull bonita@sha256:cb21f182992224f7d03dba6e5ee6a579d411f48a18fb16f40c492487b5fa4b98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.13.0` - linux; amd64

```console
$ docker pull bonita@sha256:ee74276139bf7c8a87f356b14edb98fa6bad507ff9a372aa1c605cada4649f3a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.1 MB (235082013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2ac44f6589b4a64d0ed54d539632fd9198c6e5d28d636d341ede8cf4325d306`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:04 GMT
ADD file:40290d9a94ae76c35ab1f57178130ce1c5b976e34a91e77472ecf7e945ab64f9 in / 
# Mon, 06 Jun 2022 22:21:05 GMT
CMD ["bash"]
# Mon, 06 Jun 2022 23:53:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Mon, 06 Jun 2022 23:55:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Mon, 06 Jun 2022 23:55:18 GMT
RUN mkdir /opt/custom-init.d/
# Mon, 06 Jun 2022 23:55:18 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Mon, 06 Jun 2022 23:55:21 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BONITA_VERSION
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BRANDING_VERSION
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BONITA_SHA256
# Mon, 06 Jun 2022 23:55:21 GMT
ARG BASE_URL
# Mon, 06 Jun 2022 23:55:22 GMT
ARG BONITA_URL
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_VERSION=7.13.0
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BRANDING_VERSION=2021.2-u0
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Mon, 06 Jun 2022 23:55:22 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Mon, 06 Jun 2022 23:55:22 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Mon, 06 Jun 2022 23:55:23 GMT
RUN mkdir /opt/files
# Mon, 06 Jun 2022 23:55:23 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Mon, 06 Jun 2022 23:55:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Mon, 06 Jun 2022 23:55:32 GMT
ENV HTTP_API=false
# Mon, 06 Jun 2022 23:55:32 GMT
VOLUME [/opt/bonita]
# Mon, 06 Jun 2022 23:55:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Mon, 06 Jun 2022 23:55:33 GMT
EXPOSE 8080
# Mon, 06 Jun 2022 23:55:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:09db6f815738b9c8f25420c47e093f89abaabaa653f9678587b57e8f4400b5ff`  
		Last Modified: Wed, 01 Jun 2022 21:51:21 GMT  
		Size: 26.7 MB (26711626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e1e67ee570f875ac56d020bb9ba2048a4b6afe001f2abf27cfcddb94522850b`  
		Last Modified: Mon, 06 Jun 2022 23:56:51 GMT  
		Size: 93.7 MB (93704786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c799895347844414e50219a00d72f2823de2835c43da6467690a7dfd8092c060`  
		Last Modified: Mon, 06 Jun 2022 23:56:38 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723c498ca5f2196c619a41699208691a92297201323322f46a997527f30a6f4b`  
		Last Modified: Mon, 06 Jun 2022 23:56:38 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac2f7a93399ccd26ef9ccf374b0aa06222a048a869aafe199d501d1502d94dd5`  
		Last Modified: Mon, 06 Jun 2022 23:56:37 GMT  
		Size: 930.5 KB (930477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e210e87ebbe93c80e1d898c2ed2ebdc54aca26d7a6a717cf3aa099924d61d90`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae012376ae09d981dd1cd1f1f85c7ebb4ee0e6045eb0e5db987a76209838f69f`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 3.3 KB (3301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065a8420959a3c31f08f22599784d93334ea42cfe102e8096372ce3535b744ca`  
		Last Modified: Mon, 06 Jun 2022 23:56:42 GMT  
		Size: 113.7 MB (113727928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218765ecdc92ddbb127c4fa8d00d71deeb947040f31ef34ddec95ea7cbe23676`  
		Last Modified: Mon, 06 Jun 2022 23:56:36 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:32ac0f06eb8208c29dcd8f48b6b5120f4a09c7d1986eea12c160e49f1f304d2c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.2 MB (224152225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a8d50a9b72b5d372fa2d247359ea8c16eeb9a96422b4c8639ebcd07516e652`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 01:25:07 GMT
ADD file:c562239bf6872889a22d15dda4c7dab53664b0697b60b9d09ba352b7c66719ce in / 
# Tue, 07 Jun 2022 01:25:08 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 04:36:34 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 04:38:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 04:38:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 04:38:37 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 04:38:41 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 04:38:41 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 04:38:42 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 04:38:43 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 04:38:44 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 04:38:45 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 04:38:46 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 07 Jun 2022 04:38:47 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 07 Jun 2022 04:38:48 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 07 Jun 2022 04:38:49 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 04:38:50 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 04:38:51 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 04:38:52 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 04:38:54 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 07 Jun 2022 04:39:03 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 07 Jun 2022 04:39:03 GMT
ENV HTTP_API=false
# Tue, 07 Jun 2022 04:39:04 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 04:39:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 04:39:06 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 04:39:07 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:8376114ff9b387126c379fb7f6f90b3752e3082ce48b0c727c0e1b683e1244da`  
		Last Modified: Thu, 02 Jun 2022 08:34:27 GMT  
		Size: 23.7 MB (23734664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90c2e8ebba1a8c8c808dc0fc6713296767a6225346074a494da934e5eb1bffe`  
		Last Modified: Tue, 07 Jun 2022 04:40:58 GMT  
		Size: 85.8 MB (85823076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f858118dd99d6115eb2738eae4edbabda7fcd72b175c8bbb4f39e84e990b38f`  
		Last Modified: Tue, 07 Jun 2022 04:40:46 GMT  
		Size: 122.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3cdd70aa503c2012f6c338f499d198c1fb27d4877f434e6b236fe78ea2f603c`  
		Last Modified: Tue, 07 Jun 2022 04:40:46 GMT  
		Size: 1.9 KB (1856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d206c9b11ef37af5da73286104d4d2fdc9c84521778888387ddeb57ff9e1452a`  
		Last Modified: Tue, 07 Jun 2022 04:40:45 GMT  
		Size: 859.5 KB (859531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a211292cefd1b6fa526ab765b315d54614b40a4c920cc6bd223dab23fbb99fc`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 114.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf469e907a3e246b0344a753c7c4e926f314e4ee5f49009d76b06cee65b0f93`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 3.3 KB (3304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d9c7e13abd4a2911c642e9eb0b206f5d366c496d20c9b7db27f11e69b1ab3a`  
		Last Modified: Tue, 07 Jun 2022 04:40:54 GMT  
		Size: 113.7 MB (113727876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3009fa1d28a134141a124574334d55f7cd7c043cab361fd58e9e35ef6439eeb`  
		Last Modified: Tue, 07 Jun 2022 04:40:44 GMT  
		Size: 1.7 KB (1682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.13.0` - linux; ppc64le

```console
$ docker pull bonita@sha256:b60dcfbbd19ee916cfe82496a0a3ec32704fb02d7ef614a462a8c26b419f33ee
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.6 MB (231616671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc5c514531c3d593534bda4827d79ab938f9b69604af9911b69e50720c9c5a6c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 07 Jun 2022 05:45:31 GMT
ADD file:00feca269255d07b1ddb816beb48357c556d80ab79aa81bc448abc4271d845a5 in / 
# Tue, 07 Jun 2022 05:45:36 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 10:06:17 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 07 Jun 2022 10:14:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends       curl       gnupg2       mysql-client-core-5.7       openjdk-11-jre-headless       postgresql-client       unzip       zip   && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 10:14:12 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 07 Jun 2022 10:14:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 07 Jun 2022 10:14:32 GMT
RUN gpg --keyserver keyserver.ubuntu.com --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.13/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 07 Jun 2022 10:14:35 GMT
ARG BONITA_VERSION
# Tue, 07 Jun 2022 10:14:37 GMT
ARG BRANDING_VERSION
# Tue, 07 Jun 2022 10:14:42 GMT
ARG BONITA_SHA256
# Tue, 07 Jun 2022 10:14:44 GMT
ARG BASE_URL
# Tue, 07 Jun 2022 10:14:46 GMT
ARG BONITA_URL
# Tue, 07 Jun 2022 10:14:50 GMT
ENV BONITA_VERSION=7.13.0
# Tue, 07 Jun 2022 10:14:53 GMT
ENV BRANDING_VERSION=2021.2-u0
# Tue, 07 Jun 2022 10:14:57 GMT
ENV BONITA_SHA256=e4f279765cd729885a4e353d96d1d85c5f69fef63f79183e0ccf3ffaa0cb2417
# Tue, 07 Jun 2022 10:15:00 GMT
ENV ZIP_FILE=BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 10:15:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 07 Jun 2022 10:15:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.2-u0/BonitaCommunity-2021.2-u0.zip
# Tue, 07 Jun 2022 10:15:14 GMT
RUN mkdir /opt/files
# Tue, 07 Jun 2022 10:15:15 GMT
COPY dir:6250b774ea0abc098d97c259e44608a8bf8835310bd84b47cecb5b027fb6826b in /opt/files 
# Tue, 07 Jun 2022 10:15:32 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi   && sha256sum /opt/files/${ZIP_FILE}   && echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -   && unzip -q /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip -d /opt/bonita/   && unzip /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war -d /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita/   && rm /opt/bonita/BonitaCommunity-${BRANDING_VERSION}/server/webapps/bonita.war   && rm -f /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip
# Tue, 07 Jun 2022 10:15:36 GMT
ENV HTTP_API=false
# Tue, 07 Jun 2022 10:15:42 GMT
VOLUME [/opt/bonita]
# Tue, 07 Jun 2022 10:15:45 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 07 Jun 2022 10:15:51 GMT
EXPOSE 8080
# Tue, 07 Jun 2022 10:15:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:868ede65862ecf99802bf8944efd378ff1e0751772424cea9084f390deb9f9b2`  
		Last Modified: Tue, 07 Jun 2022 05:48:49 GMT  
		Size: 30.4 MB (30442859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a331e660ead68d382742f61a8656c41551cb44956552a658c4a7b744bface060`  
		Last Modified: Tue, 07 Jun 2022 10:17:56 GMT  
		Size: 86.6 MB (86607112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a213b14ccc59baf8fae328306aad1c663e545d1071ae41070ca2f4b8407c3ce1`  
		Last Modified: Tue, 07 Jun 2022 10:17:41 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:849223db8c9360d39904a129a16fcab82cc75ed0440f6b216c84181e8eaf3a9d`  
		Last Modified: Tue, 07 Jun 2022 10:17:41 GMT  
		Size: 1.9 KB (1890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cbc038830160e8447b4c94a591d38b99d4212b0cf63674dc8d0512708ccc57`  
		Last Modified: Tue, 07 Jun 2022 10:17:39 GMT  
		Size: 831.6 KB (831568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09b68ec78a742cf1aa2513ae7a692d0fe38f63e39b8360ae6358423caa08434`  
		Last Modified: Tue, 07 Jun 2022 10:17:39 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa847ac20a1fea971cba2a4054299001b79527c44c7aee950a97916aa8a7bfb`  
		Last Modified: Tue, 07 Jun 2022 10:17:38 GMT  
		Size: 3.3 KB (3308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a42bd5762b185dffd9c65896d1caace35c218bc37c33dc07dd6f212844fbcb1`  
		Last Modified: Tue, 07 Jun 2022 10:17:49 GMT  
		Size: 113.7 MB (113727919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b94e67f1cc5eec539069c00057c5a4de04b37c4fd1b7077caca27601fc9b130`  
		Last Modified: Tue, 07 Jun 2022 10:17:38 GMT  
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
