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
