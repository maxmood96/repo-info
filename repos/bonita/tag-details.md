<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `bonita`

-	[`bonita:2021.1`](#bonita20211)
-	[`bonita:7.10`](#bonita710)
-	[`bonita:7.10.6`](#bonita7106)
-	[`bonita:7.11`](#bonita711)
-	[`bonita:7.11.4`](#bonita7114)
-	[`bonita:7.12`](#bonita712)
-	[`bonita:7.12.1`](#bonita7121)
-	[`bonita:latest`](#bonitalatest)

## `bonita:2021.1`

```console
$ docker pull bonita@sha256:cb7a169b8d659ed4d294ecd6a323aeae8a31a4b97aec0c7b3a846ea69e950db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:3096a073bce2fa66ef5d8680d8278ca722d8010f76feb50cd8eb8aefc8c95771
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237229705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a0c0a4280675453b4faa1ea3fb4888622135d364b532640233538f0bcfcabd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:47:03 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 02:47:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:47:07 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:47:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 02:47:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:47:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:47:14 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:47:14 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:47:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:47:15 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:47:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda359da4b87e70f5778d949dc8a2e01c05b0e6046622b7eff0eb4a62d41c88`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bc29cd62d12fd039bdf29b0cf9bc7aec75b765a9b3e497c3d67da30f72908`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc095c901bed978551f03662cee27979a17f11cf7e4318896537be2ebe15e7dc`  
		Last Modified: Tue, 31 Aug 2021 02:48:32 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1194914eb185a0e2dcfe5152ebb862cd9c765720c0703d5032ae75962717e916`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:722fb40422e19cc9b762111aa677d1e2a6028b3fb6b92a02fc157de8fba49897
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73389a29a1f26bbd7f43d3aff850c0dc8b76e3eb7ea5ff863f2da3b84a4a207c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:02:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:02:10 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:02:10 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:02:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:02:20 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:02:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:02:22 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:02:22 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:02:22 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e1c1c72731c590df7065975ceef09ee1266f93604e052c65bc05d913a5a4f`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84efd1951707ef2977eb51f9d9d13b2639c7a575cd001b2e058ba86249433bfa`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411f7746764319a734ea54c399b8aa2b96e5c2895ce280984676299703d7b5c`  
		Last Modified: Tue, 31 Aug 2021 03:04:00 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d20b819a0f04bddf1feecfd454f9c2bd7bdd4b2d53707272112ecae7bca420`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:32b0d47166ca68736fe0797ac6908cb1aa17970d8c4c28c5374e65c894a47775
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233848935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edded5279ca8e8bd58eea6c07ee43a8ce9fde41439b2e28411445343ce7e6fd6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:51:49 GMT
ARG BRANDING_VERSION
# Tue, 27 Jul 2021 01:51:51 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:51:53 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:51:58 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:52:00 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 27 Jul 2021 01:52:02 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 27 Jul 2021 01:52:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 27 Jul 2021 01:52:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:52:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:52:20 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:52:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 27 Jul 2021 01:52:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:52:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:52:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:52:53 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:52:56 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:53:03 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:53:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562af50260f536c102631c3e00af1641a5ef89b02d7eeb8b4f175ac07047b7b0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4549b34b465cf2aa005e75cd1344237ede2babc3e6c848ce3a94d85cb7aec0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1515dc066d8f53657c19bdf13096ba8d63b29f80bb948a9e9584ed676ceea5`  
		Last Modified: Tue, 27 Jul 2021 01:55:11 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f22fe0852be4639aef4dddb02e14e1edce7a98c01793e260a099ec9455b957`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10`

```console
$ docker pull bonita@sha256:394d45e216ab1955e45dcb522f5247ac6d4c0d7f16f5d3d4d137e039a0a57e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10` - linux; amd64

```console
$ docker pull bonita@sha256:e7ea0c4d7c1a3a3a1954ec3826381e73e52fa54b4d6c0594965dcbef4a2084cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242336189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bce3da74ac2ae038e6b299db850dfffd6c5a4eb9d25bae83eef94f62056f35`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:32 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 02:45:36 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:45:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:45:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:45:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:45:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:45:47 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:45:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:45:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 02:45:48 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 02:45:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 02:45:53 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 02:45:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 02:45:55 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:45:55 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 02:45:55 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 02:45:55 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:45:56 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113b5338edfef242ba8108e7cb8e73dfbbdd1c6090af0210b1bb470cf177785`  
		Last Modified: Tue, 31 Aug 2021 02:47:50 GMT  
		Size: 117.1 MB (117065422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5051eb4f6d463ec15e9acde49ec92c30499bbba7cd30743a6e4a1b48b97538b7`  
		Last Modified: Tue, 31 Aug 2021 02:47:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1a330f251dad8d1bf94c7f49fa22fa3da9a74b598abc3466905a17d40fd54c`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33969b7d483107e84736e89851c194cac9ddc5b62ecb73feba2d8b77aaf412b`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 576.9 KB (576941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd74c33cee47dc43924561fdedde1c84167377ab0f8d92ede3e4aacebbda7c`  
		Last Modified: Tue, 31 Aug 2021 02:47:36 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc245b5828b0e96f17df0d37e18e7903f836c389c0edaafecdc0a2450ff58c0`  
		Last Modified: Tue, 31 Aug 2021 02:47:31 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ace84dd3eb83050e4bd74047b942de1e98805507776c3d0a0e086c5a6fb01e`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:058e34528958bea10c947b162eecf600fec1bc1561d09e4647591633a8cc8f75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231037775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8fdfea1cfb1d18325253d9fb265fc65948121d71c51b0762a8a65f6e27d5f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:00:14 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 03:00:42 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:00:43 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:00:44 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:00 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:01:00 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:01:01 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:01:01 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:01:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 03:01:02 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 03:01:05 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:01:06 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:01:07 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 03:01:07 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:01:08 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 03:01:08 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 03:01:08 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:01:08 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79ac9f2e15b1e0bb60576e833601ba7abf9047cd17986fe34125af088e3902c`  
		Last Modified: Tue, 31 Aug 2021 03:03:08 GMT  
		Size: 108.8 MB (108774887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2cec2173ecb52e7fff5803915956bf4805c0d6575874fcc28ef1a12f6efabf`  
		Last Modified: Tue, 31 Aug 2021 03:02:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ead7a73f92e56f59865b34b5ba38099265022a13bb2cf10e8760f6c86cb763`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13592da4eb3367522e3527ff41e7c78d0f2fa95e68b9fe6e51e2427e36ea7470`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 547.0 KB (546966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1631fcb4f15e439779d8957a9ec3575d024b1be12fafb63d2bfed8b34a652`  
		Last Modified: Tue, 31 Aug 2021 03:02:56 GMT  
		Size: 98.0 MB (97973947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676030f6340ad8828221f37c06d208acb4171ec2b3974453d979009267061816`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c86954ea2dfa0888cdaa430f8f63534d7a8546c307287c07ea8b57718f277ac`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; ppc64le

```console
$ docker pull bonita@sha256:7435337c5b03201e08d6c5480f979dda62a5ab7a3476445b8dd29f98f7324ba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240327363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ea392201ab7d7e95ba4100cd9cda81f9c7c264c03221dad7b9da413817b785`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:40:40 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 27 Jul 2021 01:46:05 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:46:17 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:46:26 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:46:36 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:46:40 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:46:42 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:46:43 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:46:45 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:46:49 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 27 Jul 2021 01:46:53 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 27 Jul 2021 01:46:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:46:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 27 Jul 2021 01:47:06 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 27 Jul 2021 01:47:18 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 27 Jul 2021 01:47:34 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 27 Jul 2021 01:47:44 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 27 Jul 2021 01:47:46 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:47:47 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 27 Jul 2021 01:47:48 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 27 Jul 2021 01:47:50 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:47:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524c28c2164d9b09796ddd2f83322f39ef57ffb02016ebbab0f892718ed6f3c`  
		Last Modified: Tue, 27 Jul 2021 01:54:16 GMT  
		Size: 111.4 MB (111357324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c297c471637309e3e9fde7207a7fc74cd183cf576f4c0e5b76e3f773b6477d0`  
		Last Modified: Tue, 27 Jul 2021 01:53:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c51ff6961145bafb2cbf5f9fd74b019531a479ce3f5ba8be9e5cded0f0cd466`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 1.9 KB (1924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac381df1a0a13c356b1bc75f7bd3734a4f73d7d18f31502868dfe1dea35a9fe4`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44111302069faf8885ad262753b2cc3d01e90ef24c63aed05e824d857e7f3ffb`  
		Last Modified: Tue, 27 Jul 2021 01:54:03 GMT  
		Size: 98.0 MB (97973960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fc58828439256fab66ae7073d00350a28abd601e4148e168545faac8ff5e29`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d835501ba5de751fcfea8da4da19c29d17731a0cb81fc0b0110c3fbee5cdc863`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.6`

```console
$ docker pull bonita@sha256:394d45e216ab1955e45dcb522f5247ac6d4c0d7f16f5d3d4d137e039a0a57e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10.6` - linux; amd64

```console
$ docker pull bonita@sha256:e7ea0c4d7c1a3a3a1954ec3826381e73e52fa54b4d6c0594965dcbef4a2084cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.3 MB (242336189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9bce3da74ac2ae038e6b299db850dfffd6c5a4eb9d25bae83eef94f62056f35`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:44:32 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 02:45:36 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:45:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:45:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:45:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:45:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:45:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:45:47 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:45:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 02:45:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:45:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 02:45:48 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 02:45:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 02:45:53 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 02:45:55 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 02:45:55 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:45:55 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 02:45:55 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 02:45:55 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:45:56 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3113b5338edfef242ba8108e7cb8e73dfbbdd1c6090af0210b1bb470cf177785`  
		Last Modified: Tue, 31 Aug 2021 02:47:50 GMT  
		Size: 117.1 MB (117065422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5051eb4f6d463ec15e9acde49ec92c30499bbba7cd30743a6e4a1b48b97538b7`  
		Last Modified: Tue, 31 Aug 2021 02:47:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db1a330f251dad8d1bf94c7f49fa22fa3da9a74b598abc3466905a17d40fd54c`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33969b7d483107e84736e89851c194cac9ddc5b62ecb73feba2d8b77aaf412b`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 576.9 KB (576941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fd74c33cee47dc43924561fdedde1c84167377ab0f8d92ede3e4aacebbda7c`  
		Last Modified: Tue, 31 Aug 2021 02:47:36 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc245b5828b0e96f17df0d37e18e7903f836c389c0edaafecdc0a2450ff58c0`  
		Last Modified: Tue, 31 Aug 2021 02:47:31 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6ace84dd3eb83050e4bd74047b942de1e98805507776c3d0a0e086c5a6fb01e`  
		Last Modified: Tue, 31 Aug 2021 02:47:32 GMT  
		Size: 1.6 KB (1650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:058e34528958bea10c947b162eecf600fec1bc1561d09e4647591633a8cc8f75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.0 MB (231037775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8fdfea1cfb1d18325253d9fb265fc65948121d71c51b0762a8a65f6e27d5f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:00:14 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 31 Aug 2021 03:00:42 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:00:43 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:00:44 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:00 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:01:00 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:01:01 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:01:01 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 31 Aug 2021 03:01:01 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:01:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 31 Aug 2021 03:01:02 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 31 Aug 2021 03:01:05 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:01:06 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 31 Aug 2021 03:01:07 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 31 Aug 2021 03:01:07 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:01:08 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 31 Aug 2021 03:01:08 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 31 Aug 2021 03:01:08 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:01:08 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79ac9f2e15b1e0bb60576e833601ba7abf9047cd17986fe34125af088e3902c`  
		Last Modified: Tue, 31 Aug 2021 03:03:08 GMT  
		Size: 108.8 MB (108774887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2cec2173ecb52e7fff5803915956bf4805c0d6575874fcc28ef1a12f6efabf`  
		Last Modified: Tue, 31 Aug 2021 03:02:52 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2ead7a73f92e56f59865b34b5ba38099265022a13bb2cf10e8760f6c86cb763`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 1.9 KB (1915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13592da4eb3367522e3527ff41e7c78d0f2fa95e68b9fe6e51e2427e36ea7470`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 547.0 KB (546966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c1631fcb4f15e439779d8957a9ec3575d024b1be12fafb63d2bfed8b34a652`  
		Last Modified: Tue, 31 Aug 2021 03:02:56 GMT  
		Size: 98.0 MB (97973947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676030f6340ad8828221f37c06d208acb4171ec2b3974453d979009267061816`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 7.7 KB (7652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c86954ea2dfa0888cdaa430f8f63534d7a8546c307287c07ea8b57718f277ac`  
		Last Modified: Tue, 31 Aug 2021 03:02:50 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; ppc64le

```console
$ docker pull bonita@sha256:7435337c5b03201e08d6c5480f979dda62a5ab7a3476445b8dd29f98f7324ba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.3 MB (240327363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ea392201ab7d7e95ba4100cd9cda81f9c7c264c03221dad7b9da413817b785`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:40:40 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Tue, 27 Jul 2021 01:46:05 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:46:17 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:46:26 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:46:36 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:46:40 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:46:42 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:46:43 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:46:45 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:46:49 GMT
ENV BONITA_VERSION=7.10.6
# Tue, 27 Jul 2021 01:46:53 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Tue, 27 Jul 2021 01:46:54 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:46:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Tue, 27 Jul 2021 01:47:06 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Tue, 27 Jul 2021 01:47:18 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 27 Jul 2021 01:47:34 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Tue, 27 Jul 2021 01:47:44 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Tue, 27 Jul 2021 01:47:46 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:47:47 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Tue, 27 Jul 2021 01:47:48 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Tue, 27 Jul 2021 01:47:50 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:47:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0524c28c2164d9b09796ddd2f83322f39ef57ffb02016ebbab0f892718ed6f3c`  
		Last Modified: Tue, 27 Jul 2021 01:54:16 GMT  
		Size: 111.4 MB (111357324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c297c471637309e3e9fde7207a7fc74cd183cf576f4c0e5b76e3f773b6477d0`  
		Last Modified: Tue, 27 Jul 2021 01:53:56 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c51ff6961145bafb2cbf5f9fd74b019531a479ce3f5ba8be9e5cded0f0cd466`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 1.9 KB (1924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac381df1a0a13c356b1bc75f7bd3734a4f73d7d18f31502868dfe1dea35a9fe4`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 546.7 KB (546735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44111302069faf8885ad262753b2cc3d01e90ef24c63aed05e824d857e7f3ffb`  
		Last Modified: Tue, 27 Jul 2021 01:54:03 GMT  
		Size: 98.0 MB (97973960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fc58828439256fab66ae7073d00350a28abd601e4148e168545faac8ff5e29`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d835501ba5de751fcfea8da4da19c29d17731a0cb81fc0b0110c3fbee5cdc863`  
		Last Modified: Tue, 27 Jul 2021 01:53:54 GMT  
		Size: 1.7 KB (1653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:bd6030921bcd2777ed005af4ff79e4c3a7d8fcd6a872b7d446a2c3c4bf03462b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:1d1869fce833de8e5b455a38669094054c8cd09427b5ca357489c62637886919
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234162070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816da2c209ce264b46232c4703e1ad51ffd6693a51b8f262026067a2ac1cba3f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:46:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 02:46:47 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:46:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 02:46:49 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:46:49 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:46:50 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 02:46:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:46:56 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:46:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:46:58 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:46:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:46:58 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:46:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4defe4a6a79231710ca826d99cbc7d1e103e433259c7ea2e2960d29a7f824200`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e0d44bc1f45a9bda2ca8d87d5163a6da184c2fc7e8b8c192cf00f9314a559`  
		Last Modified: Tue, 31 Aug 2021 02:48:00 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca88238d657d56ad12a125d96bb6cde8dc4e650134227e7aaa7c442e931efb3`  
		Last Modified: Tue, 31 Aug 2021 02:48:07 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd44601a6feff337628a9b1fc0da6d32482b96106bc148f45e05207984807ead`  
		Last Modified: Tue, 31 Aug 2021 02:48:00 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:95092ad6b2bd314cab36257af0043c325bfab189e39dc78cb02fcd9e5decb5aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223269582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7a1321edf10188001d0c9cb9f4439c81e564dbf36bb26217f74712e2ab66b6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:01:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 03:01:47 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:01:48 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:01:49 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:01:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 03:01:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:01:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:01:54 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:01:55 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:01:55 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:01:55 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:01:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a178a891713c7a51d4cf9df12b454d83b92703fb89bdbf33c7f0e529c2c5b506`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd53216262cb919a99e340ebd9ef8c55aa355414ecab6ecb78b28ac9150b13a4`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adbd659620f4239cc11accb998730ed7530c524c4db16919ddbd8ade6df7b92`  
		Last Modified: Tue, 31 Aug 2021 03:03:32 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e3dded631ffa349cbe1698235d56e07d0aed455a74e3e3221575b1b4d78dda`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:7ce17467fcbb85e33497e8b0b03596ebb76ff0f5f1377054265f062c13990c93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230781303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ca1e3f339e3988174dde935282fbeb3c2ba5254c92a68512c469fd4c938b69`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:50:27 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:50:28 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:50:30 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:50:31 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 27 Jul 2021 01:50:32 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 27 Jul 2021 01:50:34 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 27 Jul 2021 01:50:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:50:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 27 Jul 2021 01:50:42 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:50:48 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:50:52 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 27 Jul 2021 01:51:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:51:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:51:20 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:51:23 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:51:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:51:29 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:51:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96569f8db6fc0c27d54e0b17ce10f27fa4a146eb7d3c36daee069c1544245025`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17b3820e9395f8fcca7f3e8a32db1158c904bdefb6a5521a404960cfe579ad`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e6865a3e5096e25d9be57177db42f935a66f9fa09f1be3e1631dec3afd5d82`  
		Last Modified: Tue, 27 Jul 2021 01:54:38 GMT  
		Size: 113.3 MB (113347832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c67662f3856a170290f7ab939a737d1ea97d30b90fea5a8e88468683fb53159`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:bd6030921bcd2777ed005af4ff79e4c3a7d8fcd6a872b7d446a2c3c4bf03462b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:1d1869fce833de8e5b455a38669094054c8cd09427b5ca357489c62637886919
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.2 MB (234162070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816da2c209ce264b46232c4703e1ad51ffd6693a51b8f262026067a2ac1cba3f`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:46:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 02:46:47 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 02:46:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:46:48 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 02:46:49 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:46:49 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:46:50 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 02:46:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:46:56 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:46:57 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:46:58 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:46:58 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:46:58 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:46:58 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4defe4a6a79231710ca826d99cbc7d1e103e433259c7ea2e2960d29a7f824200`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 147.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7e0d44bc1f45a9bda2ca8d87d5163a6da184c2fc7e8b8c192cf00f9314a559`  
		Last Modified: Tue, 31 Aug 2021 02:48:00 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca88238d657d56ad12a125d96bb6cde8dc4e650134227e7aaa7c442e931efb3`  
		Last Modified: Tue, 31 Aug 2021 02:48:07 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd44601a6feff337628a9b1fc0da6d32482b96106bc148f45e05207984807ead`  
		Last Modified: Tue, 31 Aug 2021 02:48:00 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:95092ad6b2bd314cab36257af0043c325bfab189e39dc78cb02fcd9e5decb5aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.3 MB (223269582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa7a1321edf10188001d0c9cb9f4439c81e564dbf36bb26217f74712e2ab66b6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:01:47 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 31 Aug 2021 03:01:47 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:01:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 31 Aug 2021 03:01:48 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:01:49 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:01:49 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 31 Aug 2021 03:01:52 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:01:53 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:01:54 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:01:55 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:01:55 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:01:55 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:01:55 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a178a891713c7a51d4cf9df12b454d83b92703fb89bdbf33c7f0e529c2c5b506`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd53216262cb919a99e340ebd9ef8c55aa355414ecab6ecb78b28ac9150b13a4`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 6.9 KB (6893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adbd659620f4239cc11accb998730ed7530c524c4db16919ddbd8ade6df7b92`  
		Last Modified: Tue, 31 Aug 2021 03:03:32 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e3dded631ffa349cbe1698235d56e07d0aed455a74e3e3221575b1b4d78dda`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:7ce17467fcbb85e33497e8b0b03596ebb76ff0f5f1377054265f062c13990c93
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.8 MB (230781303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39ca1e3f339e3988174dde935282fbeb3c2ba5254c92a68512c469fd4c938b69`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:50:27 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:50:28 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:50:30 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:50:31 GMT
ENV BONITA_VERSION=7.11.4
# Tue, 27 Jul 2021 01:50:32 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Tue, 27 Jul 2021 01:50:34 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Tue, 27 Jul 2021 01:50:36 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:50:38 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Tue, 27 Jul 2021 01:50:42 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:50:48 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:50:52 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Tue, 27 Jul 2021 01:51:04 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:51:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:51:20 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:51:23 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:51:25 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:51:29 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:51:33 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96569f8db6fc0c27d54e0b17ce10f27fa4a146eb7d3c36daee069c1544245025`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c17b3820e9395f8fcca7f3e8a32db1158c904bdefb6a5521a404960cfe579ad`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 6.9 KB (6895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e6865a3e5096e25d9be57177db42f935a66f9fa09f1be3e1631dec3afd5d82`  
		Last Modified: Tue, 27 Jul 2021 01:54:38 GMT  
		Size: 113.3 MB (113347832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c67662f3856a170290f7ab939a737d1ea97d30b90fea5a8e88468683fb53159`  
		Last Modified: Tue, 27 Jul 2021 01:54:28 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:cb7a169b8d659ed4d294ecd6a323aeae8a31a4b97aec0c7b3a846ea69e950db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:3096a073bce2fa66ef5d8680d8278ca722d8010f76feb50cd8eb8aefc8c95771
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237229705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a0c0a4280675453b4faa1ea3fb4888622135d364b532640233538f0bcfcabd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:47:03 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 02:47:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:47:07 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:47:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 02:47:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:47:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:47:14 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:47:14 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:47:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:47:15 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:47:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda359da4b87e70f5778d949dc8a2e01c05b0e6046622b7eff0eb4a62d41c88`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bc29cd62d12fd039bdf29b0cf9bc7aec75b765a9b3e497c3d67da30f72908`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc095c901bed978551f03662cee27979a17f11cf7e4318896537be2ebe15e7dc`  
		Last Modified: Tue, 31 Aug 2021 02:48:32 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1194914eb185a0e2dcfe5152ebb862cd9c765720c0703d5032ae75962717e916`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:722fb40422e19cc9b762111aa677d1e2a6028b3fb6b92a02fc157de8fba49897
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73389a29a1f26bbd7f43d3aff850c0dc8b76e3eb7ea5ff863f2da3b84a4a207c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:02:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:02:10 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:02:10 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:02:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:02:20 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:02:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:02:22 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:02:22 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:02:22 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e1c1c72731c590df7065975ceef09ee1266f93604e052c65bc05d913a5a4f`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84efd1951707ef2977eb51f9d9d13b2639c7a575cd001b2e058ba86249433bfa`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411f7746764319a734ea54c399b8aa2b96e5c2895ce280984676299703d7b5c`  
		Last Modified: Tue, 31 Aug 2021 03:04:00 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d20b819a0f04bddf1feecfd454f9c2bd7bdd4b2d53707272112ecae7bca420`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:32b0d47166ca68736fe0797ac6908cb1aa17970d8c4c28c5374e65c894a47775
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233848935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edded5279ca8e8bd58eea6c07ee43a8ce9fde41439b2e28411445343ce7e6fd6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:51:49 GMT
ARG BRANDING_VERSION
# Tue, 27 Jul 2021 01:51:51 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:51:53 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:51:58 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:52:00 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 27 Jul 2021 01:52:02 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 27 Jul 2021 01:52:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 27 Jul 2021 01:52:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:52:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:52:20 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:52:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 27 Jul 2021 01:52:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:52:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:52:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:52:53 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:52:56 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:53:03 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:53:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562af50260f536c102631c3e00af1641a5ef89b02d7eeb8b4f175ac07047b7b0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4549b34b465cf2aa005e75cd1344237ede2babc3e6c848ce3a94d85cb7aec0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1515dc066d8f53657c19bdf13096ba8d63b29f80bb948a9e9584ed676ceea5`  
		Last Modified: Tue, 27 Jul 2021 01:55:11 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f22fe0852be4639aef4dddb02e14e1edce7a98c01793e260a099ec9455b957`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:cb7a169b8d659ed4d294ecd6a323aeae8a31a4b97aec0c7b3a846ea69e950db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:3096a073bce2fa66ef5d8680d8278ca722d8010f76feb50cd8eb8aefc8c95771
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237229705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a0c0a4280675453b4faa1ea3fb4888622135d364b532640233538f0bcfcabd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:47:03 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 02:47:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:47:07 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:47:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 02:47:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:47:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:47:14 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:47:14 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:47:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:47:15 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:47:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda359da4b87e70f5778d949dc8a2e01c05b0e6046622b7eff0eb4a62d41c88`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bc29cd62d12fd039bdf29b0cf9bc7aec75b765a9b3e497c3d67da30f72908`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc095c901bed978551f03662cee27979a17f11cf7e4318896537be2ebe15e7dc`  
		Last Modified: Tue, 31 Aug 2021 02:48:32 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1194914eb185a0e2dcfe5152ebb862cd9c765720c0703d5032ae75962717e916`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:722fb40422e19cc9b762111aa677d1e2a6028b3fb6b92a02fc157de8fba49897
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73389a29a1f26bbd7f43d3aff850c0dc8b76e3eb7ea5ff863f2da3b84a4a207c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:02:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:02:10 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:02:10 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:02:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:02:20 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:02:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:02:22 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:02:22 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:02:22 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e1c1c72731c590df7065975ceef09ee1266f93604e052c65bc05d913a5a4f`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84efd1951707ef2977eb51f9d9d13b2639c7a575cd001b2e058ba86249433bfa`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411f7746764319a734ea54c399b8aa2b96e5c2895ce280984676299703d7b5c`  
		Last Modified: Tue, 31 Aug 2021 03:04:00 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d20b819a0f04bddf1feecfd454f9c2bd7bdd4b2d53707272112ecae7bca420`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:32b0d47166ca68736fe0797ac6908cb1aa17970d8c4c28c5374e65c894a47775
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233848935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edded5279ca8e8bd58eea6c07ee43a8ce9fde41439b2e28411445343ce7e6fd6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:51:49 GMT
ARG BRANDING_VERSION
# Tue, 27 Jul 2021 01:51:51 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:51:53 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:51:58 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:52:00 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 27 Jul 2021 01:52:02 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 27 Jul 2021 01:52:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 27 Jul 2021 01:52:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:52:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:52:20 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:52:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 27 Jul 2021 01:52:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:52:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:52:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:52:53 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:52:56 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:53:03 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:53:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562af50260f536c102631c3e00af1641a5ef89b02d7eeb8b4f175ac07047b7b0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4549b34b465cf2aa005e75cd1344237ede2babc3e6c848ce3a94d85cb7aec0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1515dc066d8f53657c19bdf13096ba8d63b29f80bb948a9e9584ed676ceea5`  
		Last Modified: Tue, 27 Jul 2021 01:55:11 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f22fe0852be4639aef4dddb02e14e1edce7a98c01793e260a099ec9455b957`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:cb7a169b8d659ed4d294ecd6a323aeae8a31a4b97aec0c7b3a846ea69e950db8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:3096a073bce2fa66ef5d8680d8278ca722d8010f76feb50cd8eb8aefc8c95771
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237229705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a0c0a4280675453b4faa1ea3fb4888622135d364b532640233538f0bcfcabd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:48 GMT
ADD file:425a053fd043786e9454fb269d4c93c624550fb913a8c96d03ddd430b4e6c1c3 in / 
# Tue, 31 Aug 2021 01:20:48 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:46:13 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 02:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:46:35 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 02:46:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 02:46:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 02:46:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 02:47:03 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 02:47:04 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 02:47:05 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 02:47:05 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 02:47:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 02:47:07 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 02:47:07 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 02:47:11 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 02:47:13 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 02:47:14 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 02:47:14 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 02:47:15 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 02:47:15 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 02:47:15 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:e4ca327ec0e73c737201b7a6d7b2df779a3ccf34fe9cf1b0c031e767f6464240`  
		Last Modified: Tue, 31 Aug 2021 01:22:00 GMT  
		Size: 26.7 MB (26708511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3988e14beb4269c1778e34769ab1898e483682fcbd4b467ee781dd8e2557cf`  
		Last Modified: Tue, 31 Aug 2021 02:48:16 GMT  
		Size: 93.5 MB (93519689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2707fed41459b2f8f40283aa7923322de69d79b2b94a218070601e502064716e`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55f087e25beb23f067bb1ddb19dc9cd81c49aa4610c8f29f4af000a8d0a9022`  
		Last Modified: Tue, 31 Aug 2021 02:48:03 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbe9cdad657080023b5f9fad390d964ae220d1a918a3747085c45a8fbd223cc`  
		Last Modified: Tue, 31 Aug 2021 02:48:01 GMT  
		Size: 575.3 KB (575255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dda359da4b87e70f5778d949dc8a2e01c05b0e6046622b7eff0eb4a62d41c88`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df2bc29cd62d12fd039bdf29b0cf9bc7aec75b765a9b3e497c3d67da30f72908`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 6.9 KB (6945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc095c901bed978551f03662cee27979a17f11cf7e4318896537be2ebe15e7dc`  
		Last Modified: Tue, 31 Aug 2021 02:48:32 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1194914eb185a0e2dcfe5152ebb862cd9c765720c0703d5032ae75962717e916`  
		Last Modified: Tue, 31 Aug 2021 02:48:27 GMT  
		Size: 1.7 KB (1715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:722fb40422e19cc9b762111aa677d1e2a6028b3fb6b92a02fc157de8fba49897
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226337211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73389a29a1f26bbd7f43d3aff850c0dc8b76e3eb7ea5ff863f2da3b84a4a207c`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:36 GMT
ADD file:27e3c8f7785fef80f6172954da7c3c73734c02b933dc19847e888542897d568f in / 
# Tue, 31 Aug 2021 01:40:36 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 03:01:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 31 Aug 2021 03:01:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 03:01:37 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 31 Aug 2021 03:01:38 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 31 Aug 2021 03:01:46 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 31 Aug 2021 03:01:46 GMT
ARG BONITA_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BRANDING_VERSION
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BONITA_SHA256
# Tue, 31 Aug 2021 03:02:07 GMT
ARG BASE_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ARG BONITA_URL
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 31 Aug 2021 03:02:08 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 31 Aug 2021 03:02:08 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 31 Aug 2021 03:02:09 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 31 Aug 2021 03:02:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 31 Aug 2021 03:02:10 GMT
RUN mkdir /opt/files
# Tue, 31 Aug 2021 03:02:10 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 31 Aug 2021 03:02:19 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 31 Aug 2021 03:02:20 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 31 Aug 2021 03:02:22 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 31 Aug 2021 03:02:22 GMT
VOLUME [/opt/bonita]
# Tue, 31 Aug 2021 03:02:22 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 31 Aug 2021 03:02:22 GMT
EXPOSE 8080
# Tue, 31 Aug 2021 03:02:22 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:4028d4a2ab035ee99388f4aa429a83fbaf8022de67206e9a5b69615c71069135`  
		Last Modified: Tue, 31 Aug 2021 01:42:16 GMT  
		Size: 23.7 MB (23730599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:555cb3cebbc318583a6702c2d046c45225691bddf765c968e2d284d4ce75334a`  
		Last Modified: Tue, 31 Aug 2021 03:03:40 GMT  
		Size: 85.6 MB (85635376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb991f374cd90e05d17ce87285cbce32b224ec7f2fa68d8c4e07e39229a07e42`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:561cf1765bda5eda728a2f138ba3363371a3ed4627c6502c984a469b3bc60d1e`  
		Last Modified: Tue, 31 Aug 2021 03:03:27 GMT  
		Size: 1.9 KB (1891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a72a740cdffaa3b35db0370a0929ea32b390a40bf7e06a19dfb3fe525727550`  
		Last Modified: Tue, 31 Aug 2021 03:03:25 GMT  
		Size: 545.0 KB (544982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7e1c1c72731c590df7065975ceef09ee1266f93604e052c65bc05d913a5a4f`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84efd1951707ef2977eb51f9d9d13b2639c7a575cd001b2e058ba86249433bfa`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0411f7746764319a734ea54c399b8aa2b96e5c2895ce280984676299703d7b5c`  
		Last Modified: Tue, 31 Aug 2021 03:04:00 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d20b819a0f04bddf1feecfd454f9c2bd7bdd4b2d53707272112ecae7bca420`  
		Last Modified: Tue, 31 Aug 2021 03:03:52 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:32b0d47166ca68736fe0797ac6908cb1aa17970d8c4c28c5374e65c894a47775
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233848935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edded5279ca8e8bd58eea6c07ee43a8ce9fde41439b2e28411445343ce7e6fd6`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Mon, 26 Jul 2021 23:12:31 GMT
ADD file:2e6f05bbffb47b3ea8e5e4127452e80debc89fb9e22af2dc5c735ea579adad64 in / 
# Mon, 26 Jul 2021 23:12:34 GMT
CMD ["bash"]
# Tue, 27 Jul 2021 01:48:05 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Tue, 27 Jul 2021 01:49:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Tue, 27 Jul 2021 01:50:07 GMT
RUN mkdir /opt/custom-init.d/
# Tue, 27 Jul 2021 01:50:15 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Tue, 27 Jul 2021 01:50:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Tue, 27 Jul 2021 01:50:25 GMT
ARG BONITA_VERSION
# Tue, 27 Jul 2021 01:51:49 GMT
ARG BRANDING_VERSION
# Tue, 27 Jul 2021 01:51:51 GMT
ARG BONITA_SHA256
# Tue, 27 Jul 2021 01:51:53 GMT
ARG BASE_URL
# Tue, 27 Jul 2021 01:51:58 GMT
ARG BONITA_URL
# Tue, 27 Jul 2021 01:52:00 GMT
ENV BONITA_VERSION=7.12.1
# Tue, 27 Jul 2021 01:52:02 GMT
ENV BRANDING_VERSION=2021.1
# Tue, 27 Jul 2021 01:52:06 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Tue, 27 Jul 2021 01:52:09 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:12 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Tue, 27 Jul 2021 01:52:13 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Tue, 27 Jul 2021 01:52:16 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Tue, 27 Jul 2021 01:52:20 GMT
RUN mkdir /opt/files
# Tue, 27 Jul 2021 01:52:21 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Tue, 27 Jul 2021 01:52:31 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Tue, 27 Jul 2021 01:52:41 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Tue, 27 Jul 2021 01:52:50 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Tue, 27 Jul 2021 01:52:53 GMT
VOLUME [/opt/bonita]
# Tue, 27 Jul 2021 01:52:56 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Tue, 27 Jul 2021 01:53:03 GMT
EXPOSE 8080
# Tue, 27 Jul 2021 01:53:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:3c742a0b2a0025420dcf1bc91d81de2ffb292328fad483ce715521d725503b66`  
		Last Modified: Mon, 26 Jul 2021 23:15:30 GMT  
		Size: 30.4 MB (30437958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:122e38cf8ca67c15cafbfb79b10cc63db576f58b99dc6263f8f559ece480fc98`  
		Last Modified: Tue, 27 Jul 2021 01:54:51 GMT  
		Size: 86.4 MB (86437995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0a3a3c9c04402a88e8ea2b6d49b056fcf131a881d2edadaace8b0210815457`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fefdc9fcd6ac38c5ffba630155d3fe6932b659a42bf83468548e79583d7537b`  
		Last Modified: Tue, 27 Jul 2021 01:54:32 GMT  
		Size: 1.9 KB (1883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a7810bc793a156fe6f7ab91a2bda750971a3a25fc51b31bede2b04fcac68f7`  
		Last Modified: Tue, 27 Jul 2021 01:54:29 GMT  
		Size: 546.7 KB (546729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:562af50260f536c102631c3e00af1641a5ef89b02d7eeb8b4f175ac07047b7b0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4549b34b465cf2aa005e75cd1344237ede2babc3e6c848ce3a94d85cb7aec0`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 6.9 KB (6949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1515dc066d8f53657c19bdf13096ba8d63b29f80bb948a9e9584ed676ceea5`  
		Last Modified: Tue, 27 Jul 2021 01:55:11 GMT  
		Size: 116.4 MB (116415406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f22fe0852be4639aef4dddb02e14e1edce7a98c01793e260a099ec9455b957`  
		Last Modified: Tue, 27 Jul 2021 01:55:03 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
