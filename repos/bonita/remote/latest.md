## `bonita:latest`

```console
$ docker pull bonita@sha256:fa573670c250828436bbdcf850dec5ec500b1fb1858c170bf0eaca00a14de817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:cf985e502beeda7bd213e4dc3693b5cfd446649e79cf2c0ee2a42300216dd863
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.2 MB (237233028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cb8faf747c59cd928e06fcf2203462737f87491ecd4c493d9f675a5f9c033cc`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 01 Oct 2021 02:23:23 GMT
ADD file:0d82cd095966e8ee78b593cb47a352eec842edb7bd9d9468e8a70154522447d1 in / 
# Fri, 01 Oct 2021 02:23:24 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:22:15 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Oct 2021 03:22:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:22:38 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Oct 2021 03:22:39 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Oct 2021 03:22:45 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Oct 2021 03:22:45 GMT
ARG BONITA_VERSION
# Fri, 01 Oct 2021 03:23:06 GMT
ARG BRANDING_VERSION
# Fri, 01 Oct 2021 03:23:06 GMT
ARG BONITA_SHA256
# Fri, 01 Oct 2021 03:23:06 GMT
ARG BASE_URL
# Fri, 01 Oct 2021 03:23:07 GMT
ARG BONITA_URL
# Fri, 01 Oct 2021 03:23:07 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Oct 2021 03:23:07 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Oct 2021 03:23:07 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Oct 2021 03:23:07 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Oct 2021 03:23:07 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Oct 2021 03:23:08 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Oct 2021 03:23:09 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Oct 2021 03:23:09 GMT
RUN mkdir /opt/files
# Fri, 01 Oct 2021 03:23:10 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Oct 2021 03:23:14 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Oct 2021 03:23:15 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Oct 2021 03:23:17 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Oct 2021 03:23:17 GMT
VOLUME [/opt/bonita]
# Fri, 01 Oct 2021 03:23:17 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Oct 2021 03:23:17 GMT
EXPOSE 8080
# Fri, 01 Oct 2021 03:23:18 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:284055322776031bac33723839acb0db2d063a525ba4fa1fd268a831c7553b26`  
		Last Modified: Fri, 01 Oct 2021 02:25:02 GMT  
		Size: 26.7 MB (26705075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a26e82d109872f0211374fbdd95c3c9f1799fe2afa49aee374740e411069a9`  
		Last Modified: Fri, 01 Oct 2021 03:24:22 GMT  
		Size: 93.5 MB (93524773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d98d32b0e20a905a110297e723006f1a0a3914d3c02eaa7ec1910002aca2d5b`  
		Last Modified: Fri, 01 Oct 2021 03:24:09 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a615c2a472e58e3e3ca78ee9119db9aa6cbfba55f63e200cb23320af9a9b39af`  
		Last Modified: Fri, 01 Oct 2021 03:24:09 GMT  
		Size: 1.9 KB (1881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bff023499a597e17c3b59e6fa979fc6e0c958f530d7aa8b6a5ad477d197b07`  
		Last Modified: Fri, 01 Oct 2021 03:24:06 GMT  
		Size: 576.9 KB (576940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed2f0a34ec7142b310f91d2f7ff94491fe271f681d1c0291b69c435abeba8f6`  
		Last Modified: Fri, 01 Oct 2021 03:24:33 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730994432f980a3f07c8221390194452b08adaed9fa66daa66bfc1b3a8de5e36`  
		Last Modified: Fri, 01 Oct 2021 03:24:33 GMT  
		Size: 6.9 KB (6942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627f5d7b809750eafcb136c948b160bcb2ea131f98cd825ad396179dd403dcdf`  
		Last Modified: Fri, 01 Oct 2021 03:24:38 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ef3a2fb4265fb966417cfe461e5d74bab49a20525b8cda63cb71e690843252`  
		Last Modified: Fri, 01 Oct 2021 03:24:33 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:dbde33b8607bcd5550cf36354dc50a802a53eac3ffcc3304477599273ba28e69
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.3 MB (226334004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1aa0819625c2f2587cedf8b8c4991d872594b067ebb98e96c65080d71af486`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:40 GMT
ADD file:35e2504756850fc1add00516fa89b0499b59c348457a96708eedb61313e7b25e in / 
# Fri, 01 Oct 2021 02:43:41 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:11:18 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 01 Oct 2021 03:11:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:11:40 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 01 Oct 2021 03:11:40 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 01 Oct 2021 03:11:51 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 01 Oct 2021 03:11:51 GMT
ARG BONITA_VERSION
# Fri, 01 Oct 2021 03:12:09 GMT
ARG BRANDING_VERSION
# Fri, 01 Oct 2021 03:12:10 GMT
ARG BONITA_SHA256
# Fri, 01 Oct 2021 03:12:10 GMT
ARG BASE_URL
# Fri, 01 Oct 2021 03:12:10 GMT
ARG BONITA_URL
# Fri, 01 Oct 2021 03:12:10 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 01 Oct 2021 03:12:10 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 01 Oct 2021 03:12:10 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 01 Oct 2021 03:12:11 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 01 Oct 2021 03:12:11 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 01 Oct 2021 03:12:11 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 01 Oct 2021 03:12:12 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 01 Oct 2021 03:12:12 GMT
RUN mkdir /opt/files
# Fri, 01 Oct 2021 03:12:13 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 01 Oct 2021 03:12:16 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 01 Oct 2021 03:12:17 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 01 Oct 2021 03:12:19 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 01 Oct 2021 03:12:19 GMT
VOLUME [/opt/bonita]
# Fri, 01 Oct 2021 03:12:19 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 01 Oct 2021 03:12:19 GMT
EXPOSE 8080
# Fri, 01 Oct 2021 03:12:19 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:f46992f278c2dd50c481ff60ce8528b6eb59016ac6243e1a7fb385c79c5944b9`  
		Last Modified: Fri, 01 Oct 2021 02:45:30 GMT  
		Size: 23.7 MB (23727476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f2961f2a4bb67da5eacd8035656d46b0b9ce152f747e5a4866615a41912e77`  
		Last Modified: Fri, 01 Oct 2021 03:13:29 GMT  
		Size: 85.6 MB (85633335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbadb494c476cbc9027d808b5602ca944569d12f137a0d2ecdd29df277acd0e6`  
		Last Modified: Fri, 01 Oct 2021 03:13:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6f264659a1637719775ef2123464f83436ff5bb0548fc6dcfd79901ac8c637`  
		Last Modified: Fri, 01 Oct 2021 03:13:16 GMT  
		Size: 1.9 KB (1886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d568262d6dd7434b5917a08133c89776d2f316d5fe0322f20f5c224daf1fd3`  
		Last Modified: Fri, 01 Oct 2021 03:13:14 GMT  
		Size: 547.0 KB (546951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96344b1ed8fdc3a7e4c6982958db4e3db69e1c243b99a310d69c2a647186d799`  
		Last Modified: Fri, 01 Oct 2021 03:13:40 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a80275c26cbf501b20ec3280ac760bc2d08edfd02c4bfbc5883f9203f0aa8d`  
		Last Modified: Fri, 01 Oct 2021 03:13:40 GMT  
		Size: 6.9 KB (6938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2236e483c06abc6f1a2ad6cc261ce0ef609048f07ba63ff4f6809d6a9fdc49`  
		Last Modified: Fri, 01 Oct 2021 03:13:47 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77ed7af5efb5ad02a38247d168986cfbd102e6db255f183e4a2f19bbd5c430a8`  
		Last Modified: Fri, 01 Oct 2021 03:13:40 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:ac1416c77bcac78a9298a94a94abbefde6a84f30d1c8c6ddb9d974813850e64d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.8 MB (233842751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39f570d1f0ea23c7cb3e2af3d23faa36d28d1e857626b870b352bb5bed8d9921`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Tue, 05 Oct 2021 11:07:29 GMT
ADD file:fd96554dfb72307c3cf9292c343050a8b9f0848735b7555820f0068914ebd758 in / 
# Tue, 05 Oct 2021 11:07:35 GMT
CMD ["bash"]
# Wed, 06 Oct 2021 17:43:30 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Wed, 06 Oct 2021 17:46:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Wed, 06 Oct 2021 17:46:47 GMT
RUN mkdir /opt/custom-init.d/
# Wed, 06 Oct 2021 17:46:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Wed, 06 Oct 2021 17:47:20 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Wed, 06 Oct 2021 17:47:24 GMT
ARG BONITA_VERSION
# Wed, 06 Oct 2021 17:49:45 GMT
ARG BRANDING_VERSION
# Wed, 06 Oct 2021 17:49:48 GMT
ARG BONITA_SHA256
# Wed, 06 Oct 2021 17:49:51 GMT
ARG BASE_URL
# Wed, 06 Oct 2021 17:49:55 GMT
ARG BONITA_URL
# Wed, 06 Oct 2021 17:50:00 GMT
ENV BONITA_VERSION=7.12.1
# Wed, 06 Oct 2021 17:50:05 GMT
ENV BRANDING_VERSION=2021.1
# Wed, 06 Oct 2021 17:50:10 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Wed, 06 Oct 2021 17:50:17 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Wed, 06 Oct 2021 17:50:21 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Wed, 06 Oct 2021 17:50:24 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Wed, 06 Oct 2021 17:50:33 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Wed, 06 Oct 2021 17:50:46 GMT
RUN mkdir /opt/files
# Wed, 06 Oct 2021 17:50:49 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Wed, 06 Oct 2021 17:51:23 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Wed, 06 Oct 2021 17:51:49 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Wed, 06 Oct 2021 17:52:20 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Wed, 06 Oct 2021 17:52:34 GMT
VOLUME [/opt/bonita]
# Wed, 06 Oct 2021 17:52:38 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Wed, 06 Oct 2021 17:52:43 GMT
EXPOSE 8080
# Wed, 06 Oct 2021 17:52:52 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:db28fc1e594e5598e665c54ac1b7fd602d86dddaf8bb237a72303cec22a9185c`  
		Last Modified: Tue, 05 Oct 2021 11:10:31 GMT  
		Size: 30.4 MB (30432921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b3edc21cfc352b7713634c746e33cbc4fa7e3ca0a6a30ff4b38e53392c9b32`  
		Last Modified: Wed, 06 Oct 2021 17:54:27 GMT  
		Size: 86.4 MB (86436862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a018aca2fc40ed2d9ef571ad40cece30b4b96114ea033190abeebc6b26f1159a`  
		Last Modified: Wed, 06 Oct 2021 17:54:13 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b1a43207f8aeb2bffccebb563d56f146a642348a74c917fccedc5406ff7c048`  
		Last Modified: Wed, 06 Oct 2021 17:54:13 GMT  
		Size: 1.9 KB (1882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944db579c4969b5a1590926d71763dcdeff12d81aa7bc74411ea87c3999aa9c9`  
		Last Modified: Wed, 06 Oct 2021 17:54:11 GMT  
		Size: 546.7 KB (546726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30bb1157a2d16356c3fe03471316decff49b6dc50796a886d2fb6537ec3c3b21`  
		Last Modified: Wed, 06 Oct 2021 17:54:39 GMT  
		Size: 146.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3c397b4e693ea0a648aa5d5d11a1d68a1688c3894e594755a4c7b9ab141155`  
		Last Modified: Wed, 06 Oct 2021 17:54:39 GMT  
		Size: 6.9 KB (6944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd833d0ae3726dfae569704a9b090ee2eb0dc552d22117765785b6bfbc7a682f`  
		Last Modified: Wed, 06 Oct 2021 17:54:48 GMT  
		Size: 116.4 MB (116415402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c02458dc3f64372d814c185b974e07b342eec4c2dabd730f6e29a0f1e1b7d56`  
		Last Modified: Wed, 06 Oct 2021 17:54:39 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
