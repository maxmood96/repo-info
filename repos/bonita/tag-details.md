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
$ docker pull bonita@sha256:1bb3971e7fb1b18c92b6b0bada9c8b3df0b392051789b9062f1907e39892ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:2021.1` - linux; amd64

```console
$ docker pull bonita@sha256:bec7c62bfa26447c37ea9a71f638671f52400db14f9229eeee8e7df6a6a299b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238893974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce2c8eced3ba09353d4f974632f31ecce2489fc06865b589740531b2abbd1d3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:54:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 09:54:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:54:35 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 09:54:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 09:54:38 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 09:54:57 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 09:54:57 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 09:54:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 09:54:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 09:54:59 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 09:55:00 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 09:55:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 09:55:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 09:55:07 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 09:55:09 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 09:55:09 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 09:55:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 09:55:09 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 09:55:09 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e534248c77c94586396089f5fe1e6ef3445619f3b25b01e3788c31a39246de`  
		Last Modified: Fri, 26 Mar 2021 09:56:17 GMT  
		Size: 95.2 MB (95182928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51fffa5c2969e00e61b80759c01c7b29a445487471b69cab746c2912685b51`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0795bb218aad676992e4855a54a7a8fbf0139bdb13b12a54e94c512da7714`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef20992b153c738c647dc0b493b155dc50a750365be70fcf88cfe88ce28b63d`  
		Last Modified: Fri, 26 Mar 2021 09:56:00 GMT  
		Size: 573.0 KB (572988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab13c0cfd407a99af4475a201b0e82ef59eb70270e887c1d76519a390f6df46`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fef7e4f41959abb0200ce52dbf1df79a3a1c6e2135817fa0b950601145d24a`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa40d92e0791bad639df8e2c95739cc01e6fc08a1c47bac8675668516852dba`  
		Last Modified: Fri, 26 Mar 2021 09:56:37 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4dbd4b7563e31dcb93c41f4ddce6c2216761188046dc480a97cd1199207e72`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:84030597fea55c49a48a9eed24ac7eda2edb032d525d4cf0ccd9d04abc1149a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226973813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821bd2f3d2ce3bc73a3dcf96a4de7947e6474c1ea9878f60436f6cbf347e71ac`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:06:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 14:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:07:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 14:07:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 14:07:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 14:07:24 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 14:08:18 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 14:08:19 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 14:08:20 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 14:08:21 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 14:08:21 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 14:08:22 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 14:08:23 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 14:08:24 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 14:08:25 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 14:08:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 14:08:34 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 14:08:36 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 14:08:37 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 14:08:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 14:08:46 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 14:08:51 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 14:08:52 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 14:08:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 14:08:56 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 14:08:57 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5c85b2acaf4dee357935720ab250421d16571fef3e471780b122f2cdf83af`  
		Last Modified: Fri, 26 Mar 2021 14:10:17 GMT  
		Size: 86.3 MB (86271251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c2fdd692d74aaecc195ddf2db73f8559e338bead6fea0723ebf300f960e59`  
		Last Modified: Fri, 26 Mar 2021 14:09:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bcf42f29aedf6bbe85cc51f150084420ac531553a9612c2f879ee3bd0078f`  
		Last Modified: Fri, 26 Mar 2021 14:09:57 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e49ab418707059be0c1d66745b5321be3a596a356b98745231078ea5c4a0f98`  
		Last Modified: Fri, 26 Mar 2021 14:09:56 GMT  
		Size: 542.5 KB (542478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa07e9e63eacc299ff02c8c939a04a38e581f5885ed74953fa8dcbd9a11e27`  
		Last Modified: Fri, 26 Mar 2021 14:10:26 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03afcbb1b94d8b23243e19af274991ce7d143eec99fc30a3b905d442cd576aaa`  
		Last Modified: Fri, 26 Mar 2021 14:10:25 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae05ebc2888a5b8cd66f45562ad4677e9b984afc66311d568431230557f8f1b4`  
		Last Modified: Fri, 26 Mar 2021 14:10:37 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cee0632a7f0f0e126c55e70fab96fa8540c079acd2d96380460c09dc2705374`  
		Last Modified: Fri, 26 Mar 2021 14:10:25 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:2021.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:b212334198bfe535cb9fa6a435e38796b9a47a4a043346a23bd772588b3f9488
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234579781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d51c75ce92943c2cbd2bf2cfa58b039d33b7c95022893f681a1677e52866bef`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:54:50 GMT
ADD file:16a7a25947f319127d6b6ca6c99ff4e36bc4112c64ed67d2678b949eea2ad7e9 in / 
# Thu, 25 Mar 2021 22:56:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:59:22 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 16:57:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 17:00:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:01:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 17:01:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 17:01:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 17:01:47 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 17:05:04 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 17:05:13 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 17:05:20 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 17:05:22 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 17:05:29 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 17:05:32 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 17:05:38 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 17:05:45 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 17:05:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 17:05:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 17:06:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 17:06:16 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 17:06:18 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 17:06:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 17:06:48 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 17:07:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 17:07:06 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 17:07:08 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 17:07:14 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 17:07:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:5ade347cf74df0ad62b82c57b0a6f0411ef9ecad9336a99c9e116ee5d1ff3d82`  
		Last Modified: Thu, 25 Mar 2021 23:15:40 GMT  
		Size: 30.4 MB (30423262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918394a3ae216a0c5018f2cb9895614a0b9689fca3efc24700f5e1b1866273ad`  
		Last Modified: Thu, 25 Mar 2021 23:15:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dcfbdd713e2165e8011c88e37ddcbc43523f8f06ee41b65fa9edf100f0cebc`  
		Last Modified: Fri, 26 Mar 2021 17:08:55 GMT  
		Size: 87.2 MB (87187374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7279cfc51feea32c6ce6ff6a7154c575e7d99a4fa22398ed8ec8a463e63c656b`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdde82b9d378f4b5dbc93460991eef8e85aa8fb50a6ac82dc50241dcf3324538`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dace4db6d23b69db02a954695ce320a7335cf6ef057d6d7bbd09123f56acda`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 541.8 KB (541849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107b99fec4b745157230b018539d14317dbf688634bab8a5c5b96c6c9da5206`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfd93428c77e1a39586ba0191b041dee349e2c444aaa68bab9b0eccbb62ae0`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332474a1847cac1f6d92aff976376e8781b200ea908f7e4bf41159e720c03202`  
		Last Modified: Fri, 26 Mar 2021 17:09:18 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0660aed029edb19c64bdb515578304dc1c653850bd654b97072f9db68a8c2bf`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10`

```console
$ docker pull bonita@sha256:28b337f4d203e94042a28c2eaa1223c6fc1fdafd9c89b059e2bf5ca3c5c8144f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10` - linux; amd64

```console
$ docker pull bonita@sha256:68c1b07825e2b49ec7e2f5d09d0bb9cb1124dd5cd413e04990f43769902a6742
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243983655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b247e4e0e753c3f92e346681550706afe418876d318ef882dfd1e7c6a2c9956`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:52:33 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 26 Mar 2021 09:53:56 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:53:57 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 09:53:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 09:54:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 09:54:01 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 09:54:01 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 09:54:01 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 09:54:01 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 09:54:01 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 26 Mar 2021 09:54:01 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 26 Mar 2021 09:54:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 09:54:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 26 Mar 2021 09:54:03 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 26 Mar 2021 09:54:06 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 09:54:08 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 09:54:09 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 26 Mar 2021 09:54:09 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 09:54:10 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 26 Mar 2021 09:54:10 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 26 Mar 2021 09:54:10 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 09:54:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758aa4bda331f1a79eeaa9ef209ea761536760099648e00edb1dc97da5cbab99`  
		Last Modified: Fri, 26 Mar 2021 09:55:45 GMT  
		Size: 118.7 MB (118713514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0288caa263e5157f91590e85aaf9bc0137e0a6b9cc17c40fea8e82bf7a8026`  
		Last Modified: Fri, 26 Mar 2021 09:55:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e783d95bec0ad604e56da21bd7a41ff9e8e5eec5154dc13ce6136a5cddb491ff`  
		Last Modified: Fri, 26 Mar 2021 09:55:26 GMT  
		Size: 1.9 KB (1909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ac2c18c4374d15acff76cd5f82ef507fec3cd3843175a5d5a34c42eca5d839`  
		Last Modified: Fri, 26 Mar 2021 09:55:27 GMT  
		Size: 573.0 KB (572991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cccb95ba60806e8bd9f1abd297ea7c30e082e5d40416583f8f1fb7a4452986`  
		Last Modified: Fri, 26 Mar 2021 09:55:30 GMT  
		Size: 98.0 MB (97973960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d07ada1cef794cb91ebc12c7b9e8c144b323aa8b2607160f2341bea2648b96`  
		Last Modified: Fri, 26 Mar 2021 09:55:25 GMT  
		Size: 7.7 KB (7654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5427824d2e3e2398968d0bdcdcc2b7a9d23bbe2b9e61bcfe2e8c6a587d9e8898`  
		Last Modified: Fri, 26 Mar 2021 09:55:27 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5960d0e66b149a4ec53209af871122aa865b1b66aaf8ee64aff584e3e8d9e8f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231693193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96552e7729f9a0490503cadf14561a2a3be29464277b02873b57f071786a4eba`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:03:54 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 26 Mar 2021 14:05:18 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:05:25 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 14:05:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 14:05:34 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 14:05:36 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 14:05:37 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 14:05:38 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 14:05:40 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 14:05:41 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 26 Mar 2021 14:05:42 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 26 Mar 2021 14:05:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 14:05:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 26 Mar 2021 14:05:46 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 26 Mar 2021 14:05:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 14:05:56 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 14:06:00 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 26 Mar 2021 14:06:01 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 14:06:02 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 26 Mar 2021 14:06:04 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 26 Mar 2021 14:06:05 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 14:06:07 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678795cf428162a64b54fe3128aeb3cd065caffeb94422d28d810d48f0e8f955`  
		Last Modified: Fri, 26 Mar 2021 14:09:47 GMT  
		Size: 109.4 MB (109431563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e88b9615c3c34492d78d6c784bb7d9fe17e5850fc8e8fc54abe7868271a752e`  
		Last Modified: Fri, 26 Mar 2021 14:09:23 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a717182232e648aa8d3d3920e676485d8d1886fefffed930a180edc9591713`  
		Last Modified: Fri, 26 Mar 2021 14:09:22 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c87c87e0d2248b5be0ca62331a729dcbddd5700dd69d5e6348c86d8931f11e`  
		Last Modified: Fri, 26 Mar 2021 14:09:21 GMT  
		Size: 542.5 KB (542481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70bd8bce850f15279ee5709dcf99a47bdda16648af16a5a9502cfd0aa5bab57`  
		Last Modified: Fri, 26 Mar 2021 14:09:31 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd01e4f65394f7c9b6bf509a7ac5fe45738f411125eb46cd063a192617d9f482`  
		Last Modified: Fri, 26 Mar 2021 14:09:21 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39558b0dee2fd44196c80e02961b2f8fd67ab517b0ef3e89c035d9d67200c8c`  
		Last Modified: Fri, 26 Mar 2021 14:09:21 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10` - linux; ppc64le

```console
$ docker pull bonita@sha256:2405e8c31dde0e0b28445d72ca6b2a17b4a78061749155cdd2e67190d5202b84
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241065670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735fb1c434bf5c3956d9037a6d8d41df14f1f7631cade530d3aca0e88890b21a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:54:50 GMT
ADD file:16a7a25947f319127d6b6ca6c99ff4e36bc4112c64ed67d2678b949eea2ad7e9 in / 
# Thu, 25 Mar 2021 22:56:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:59:22 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 16:48:49 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 26 Mar 2021 16:54:50 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 16:54:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 16:55:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 16:55:19 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 16:55:24 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 16:55:28 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 16:55:34 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 16:55:42 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 16:55:47 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 26 Mar 2021 16:55:51 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 26 Mar 2021 16:55:53 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 16:55:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 26 Mar 2021 16:56:02 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 26 Mar 2021 16:56:12 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 16:56:21 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 16:56:36 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 26 Mar 2021 16:56:40 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 16:56:42 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 26 Mar 2021 16:56:45 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 26 Mar 2021 16:56:47 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 16:56:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:5ade347cf74df0ad62b82c57b0a6f0411ef9ecad9336a99c9e116ee5d1ff3d82`  
		Last Modified: Thu, 25 Mar 2021 23:15:40 GMT  
		Size: 30.4 MB (30423262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918394a3ae216a0c5018f2cb9895614a0b9689fca3efc24700f5e1b1866273ad`  
		Last Modified: Thu, 25 Mar 2021 23:15:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5b81938deae47fb0dbc6f4ec2f107f645f33c0e019d6af9ddda9b99dd8732a`  
		Last Modified: Fri, 26 Mar 2021 17:08:21 GMT  
		Size: 112.1 MB (112114198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf1b4529a13eacbcf82e707e3c387bd0170d155f339ee583cee8d16f0bcef24`  
		Last Modified: Fri, 26 Mar 2021 17:07:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53453f0690ac645be2f279359d41138b5664f414b5839d84f0a0e8bbb2cd876e`  
		Last Modified: Fri, 26 Mar 2021 17:07:53 GMT  
		Size: 1.9 KB (1912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4b1bc7e8c572212bda3e6a9cbc16e9aa80d64177f28b2a9bd3fff450d24998`  
		Last Modified: Fri, 26 Mar 2021 17:07:53 GMT  
		Size: 541.8 KB (541848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b82248a33adadd2e224ee14484da77b191ec6557ae7cc185f931ec9bfa50fd`  
		Last Modified: Fri, 26 Mar 2021 17:08:01 GMT  
		Size: 98.0 MB (97973947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f639522ef9249bd2c35432e7c19008b3bf85d840906ba37a39c3a485b85dd589`  
		Last Modified: Fri, 26 Mar 2021 17:07:53 GMT  
		Size: 7.7 KB (7657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be7e6acd47eb04c5a8912e2caa67e4181634d5b4e4b4458cf55b43a17fff6cd`  
		Last Modified: Fri, 26 Mar 2021 17:07:53 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.10.6`

```console
$ docker pull bonita@sha256:28b337f4d203e94042a28c2eaa1223c6fc1fdafd9c89b059e2bf5ca3c5c8144f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.10.6` - linux; amd64

```console
$ docker pull bonita@sha256:68c1b07825e2b49ec7e2f5d09d0bb9cb1124dd5cd413e04990f43769902a6742
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.0 MB (243983655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b247e4e0e753c3f92e346681550706afe418876d318ef882dfd1e7c6a2c9956`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:52:33 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 26 Mar 2021 09:53:56 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:53:57 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 09:53:58 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 09:54:00 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 09:54:01 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 09:54:01 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 09:54:01 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 09:54:01 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 09:54:01 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 26 Mar 2021 09:54:01 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 26 Mar 2021 09:54:02 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 09:54:02 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 26 Mar 2021 09:54:03 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 26 Mar 2021 09:54:06 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 09:54:08 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 09:54:09 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 26 Mar 2021 09:54:09 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 09:54:10 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 26 Mar 2021 09:54:10 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 26 Mar 2021 09:54:10 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 09:54:10 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758aa4bda331f1a79eeaa9ef209ea761536760099648e00edb1dc97da5cbab99`  
		Last Modified: Fri, 26 Mar 2021 09:55:45 GMT  
		Size: 118.7 MB (118713514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e0288caa263e5157f91590e85aaf9bc0137e0a6b9cc17c40fea8e82bf7a8026`  
		Last Modified: Fri, 26 Mar 2021 09:55:27 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e783d95bec0ad604e56da21bd7a41ff9e8e5eec5154dc13ce6136a5cddb491ff`  
		Last Modified: Fri, 26 Mar 2021 09:55:26 GMT  
		Size: 1.9 KB (1909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29ac2c18c4374d15acff76cd5f82ef507fec3cd3843175a5d5a34c42eca5d839`  
		Last Modified: Fri, 26 Mar 2021 09:55:27 GMT  
		Size: 573.0 KB (572991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cccb95ba60806e8bd9f1abd297ea7c30e082e5d40416583f8f1fb7a4452986`  
		Last Modified: Fri, 26 Mar 2021 09:55:30 GMT  
		Size: 98.0 MB (97973960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17d07ada1cef794cb91ebc12c7b9e8c144b323aa8b2607160f2341bea2648b96`  
		Last Modified: Fri, 26 Mar 2021 09:55:25 GMT  
		Size: 7.7 KB (7654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5427824d2e3e2398968d0bdcdcc2b7a9d23bbe2b9e61bcfe2e8c6a587d9e8898`  
		Last Modified: Fri, 26 Mar 2021 09:55:27 GMT  
		Size: 1.7 KB (1651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:5960d0e66b149a4ec53209af871122aa865b1b66aaf8ee64aff584e3e8d9e8f1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.7 MB (231693193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96552e7729f9a0490503cadf14561a2a3be29464277b02873b57f071786a4eba`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:03:54 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 26 Mar 2021 14:05:18 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:05:25 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 14:05:28 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 14:05:34 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 14:05:36 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 14:05:37 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 14:05:38 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 14:05:40 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 14:05:41 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 26 Mar 2021 14:05:42 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 26 Mar 2021 14:05:43 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 14:05:44 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 26 Mar 2021 14:05:46 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 26 Mar 2021 14:05:52 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 14:05:56 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 14:06:00 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 26 Mar 2021 14:06:01 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 14:06:02 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 26 Mar 2021 14:06:04 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 26 Mar 2021 14:06:05 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 14:06:07 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678795cf428162a64b54fe3128aeb3cd065caffeb94422d28d810d48f0e8f955`  
		Last Modified: Fri, 26 Mar 2021 14:09:47 GMT  
		Size: 109.4 MB (109431563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e88b9615c3c34492d78d6c784bb7d9fe17e5850fc8e8fc54abe7868271a752e`  
		Last Modified: Fri, 26 Mar 2021 14:09:23 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a717182232e648aa8d3d3920e676485d8d1886fefffed930a180edc9591713`  
		Last Modified: Fri, 26 Mar 2021 14:09:22 GMT  
		Size: 1.9 KB (1911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c87c87e0d2248b5be0ca62331a729dcbddd5700dd69d5e6348c86d8931f11e`  
		Last Modified: Fri, 26 Mar 2021 14:09:21 GMT  
		Size: 542.5 KB (542481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70bd8bce850f15279ee5709dcf99a47bdda16648af16a5a9502cfd0aa5bab57`  
		Last Modified: Fri, 26 Mar 2021 14:09:31 GMT  
		Size: 98.0 MB (97973946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd01e4f65394f7c9b6bf509a7ac5fe45738f411125eb46cd063a192617d9f482`  
		Last Modified: Fri, 26 Mar 2021 14:09:21 GMT  
		Size: 7.7 KB (7653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39558b0dee2fd44196c80e02961b2f8fd67ab517b0ef3e89c035d9d67200c8c`  
		Last Modified: Fri, 26 Mar 2021 14:09:21 GMT  
		Size: 1.7 KB (1654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.10.6` - linux; ppc64le

```console
$ docker pull bonita@sha256:2405e8c31dde0e0b28445d72ca6b2a17b4a78061749155cdd2e67190d5202b84
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.1 MB (241065670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735fb1c434bf5c3956d9037a6d8d41df14f1f7631cade530d3aca0e88890b21a`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:54:50 GMT
ADD file:16a7a25947f319127d6b6ca6c99ff4e36bc4112c64ed67d2678b949eea2ad7e9 in / 
# Thu, 25 Mar 2021 22:56:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:59:22 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 16:48:49 GMT
MAINTAINER Jérémy Jacquier-Roux <jeremy.jacquier-roux@bonitasoft.org>
# Fri, 26 Mar 2021 16:54:50 GMT
RUN apt-get update && apt-get install -y   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 16:54:59 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 16:55:06 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 16:55:19 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 16:55:24 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 16:55:28 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 16:55:34 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 16:55:42 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 16:55:47 GMT
ENV BONITA_VERSION=7.10.6
# Fri, 26 Mar 2021 16:55:51 GMT
ENV BONITA_SHA256=aaf61a044e7a8d9ec95d2b5d0c315a6d01d9c93ba01d753fcb008e2cfbbb725f
# Fri, 26 Mar 2021 16:55:53 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 16:55:55 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.10.6/BonitaCommunity-7.10.6.zip
# Fri, 26 Mar 2021 16:56:02 GMT
RUN echo "Downloading Bonita from url: $BONITA_URL"
# Fri, 26 Mar 2021 16:56:12 GMT
RUN mkdir /opt/files   && curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 16:56:21 GMT
RUN sha256sum /opt/files/BonitaCommunity-${BONITA_VERSION}.zip
# Fri, 26 Mar 2021 16:56:36 GMT
RUN echo "$BONITA_SHA256" /opt/files/BonitaCommunity-${BONITA_VERSION}.zip | sha256sum -c -
# Fri, 26 Mar 2021 16:56:40 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 16:56:42 GMT
COPY dir:46816633cc37ba9fd23af260c8c2384c15f3b4385b5752d6b42577967959f7f0 in /opt/files 
# Fri, 26 Mar 2021 16:56:45 GMT
COPY dir:157c135edc1215565cc6815861e1a1728bdf09f6cfceca03c1639b2262f1cd65 in /opt/templates 
# Fri, 26 Mar 2021 16:56:47 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 16:56:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:5ade347cf74df0ad62b82c57b0a6f0411ef9ecad9336a99c9e116ee5d1ff3d82`  
		Last Modified: Thu, 25 Mar 2021 23:15:40 GMT  
		Size: 30.4 MB (30423262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918394a3ae216a0c5018f2cb9895614a0b9689fca3efc24700f5e1b1866273ad`  
		Last Modified: Thu, 25 Mar 2021 23:15:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5b81938deae47fb0dbc6f4ec2f107f645f33c0e019d6af9ddda9b99dd8732a`  
		Last Modified: Fri, 26 Mar 2021 17:08:21 GMT  
		Size: 112.1 MB (112114198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bf1b4529a13eacbcf82e707e3c387bd0170d155f339ee583cee8d16f0bcef24`  
		Last Modified: Fri, 26 Mar 2021 17:07:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53453f0690ac645be2f279359d41138b5664f414b5839d84f0a0e8bbb2cd876e`  
		Last Modified: Fri, 26 Mar 2021 17:07:53 GMT  
		Size: 1.9 KB (1912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4b1bc7e8c572212bda3e6a9cbc16e9aa80d64177f28b2a9bd3fff450d24998`  
		Last Modified: Fri, 26 Mar 2021 17:07:53 GMT  
		Size: 541.8 KB (541848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b82248a33adadd2e224ee14484da77b191ec6557ae7cc185f931ec9bfa50fd`  
		Last Modified: Fri, 26 Mar 2021 17:08:01 GMT  
		Size: 98.0 MB (97973947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f639522ef9249bd2c35432e7c19008b3bf85d840906ba37a39c3a485b85dd589`  
		Last Modified: Fri, 26 Mar 2021 17:07:53 GMT  
		Size: 7.7 KB (7657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be7e6acd47eb04c5a8912e2caa67e4181634d5b4e4b4458cf55b43a17fff6cd`  
		Last Modified: Fri, 26 Mar 2021 17:07:53 GMT  
		Size: 1.7 KB (1652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11`

```console
$ docker pull bonita@sha256:bea03469bae4d92ca9a760d5ad452fbb4b7cb74393979e0b29f6e09b6ab62337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11` - linux; amd64

```console
$ docker pull bonita@sha256:b694e19ef9ac650a23887d2c22c36276b9f48993eed040886e30b147c9b88ea8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235826347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1d641447e311f7e0cd7a0dd4672a56e5d7c6d2a49334a909ee29f9f41cf6fd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:54:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 09:54:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:54:35 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 09:54:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 09:54:38 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 09:54:39 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 26 Mar 2021 09:54:39 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 26 Mar 2021 09:54:39 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 09:54:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 09:54:39 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 09:54:40 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 09:54:41 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 09:54:41 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 26 Mar 2021 09:54:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 26 Mar 2021 09:54:49 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 09:54:51 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 09:54:51 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 09:54:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 09:54:51 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 09:54:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e534248c77c94586396089f5fe1e6ef3445619f3b25b01e3788c31a39246de`  
		Last Modified: Fri, 26 Mar 2021 09:56:17 GMT  
		Size: 95.2 MB (95182928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51fffa5c2969e00e61b80759c01c7b29a445487471b69cab746c2912685b51`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0795bb218aad676992e4855a54a7a8fbf0139bdb13b12a54e94c512da7714`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef20992b153c738c647dc0b493b155dc50a750365be70fcf88cfe88ce28b63d`  
		Last Modified: Fri, 26 Mar 2021 09:56:00 GMT  
		Size: 573.0 KB (572988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2342ed4cdb3bb862f5ee7bebbc9876f88377e7143203e1d9356aa2ad597373dc`  
		Last Modified: Fri, 26 Mar 2021 09:55:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8ade80e567ac70f7da85f2303331a1637cb679e23c1c02fcd30ad8b60fc5ea`  
		Last Modified: Fri, 26 Mar 2021 09:55:59 GMT  
		Size: 6.9 KB (6891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e4b5d9808791fa19090b61806ed17ea0c9fdc6a9d0f96f815830d9fe297251`  
		Last Modified: Fri, 26 Mar 2021 09:56:05 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfb68eeef2f54c5a0c542b65ba7fc90440c48b38740396b882c0e8d356613cb`  
		Last Modified: Fri, 26 Mar 2021 09:55:59 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:595db97e2cf776906c9ddce8d546636495feefcad54433725011a05e0dff57c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223906185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac3ea304f138a40bf1efa2960c4dc1fc106e954dd178a5bf2af20463bc846a5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:06:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 14:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:07:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 14:07:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 14:07:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 14:07:24 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 14:07:25 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 14:07:26 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 14:07:28 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 14:07:30 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 26 Mar 2021 14:07:31 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 26 Mar 2021 14:07:33 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 14:07:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 14:07:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 14:07:41 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 14:07:45 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 14:07:47 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 26 Mar 2021 14:07:55 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 26 Mar 2021 14:07:59 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 14:08:03 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 14:08:04 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 14:08:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 14:08:08 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 14:08:09 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5c85b2acaf4dee357935720ab250421d16571fef3e471780b122f2cdf83af`  
		Last Modified: Fri, 26 Mar 2021 14:10:17 GMT  
		Size: 86.3 MB (86271251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c2fdd692d74aaecc195ddf2db73f8559e338bead6fea0723ebf300f960e59`  
		Last Modified: Fri, 26 Mar 2021 14:09:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bcf42f29aedf6bbe85cc51f150084420ac531553a9612c2f879ee3bd0078f`  
		Last Modified: Fri, 26 Mar 2021 14:09:57 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e49ab418707059be0c1d66745b5321be3a596a356b98745231078ea5c4a0f98`  
		Last Modified: Fri, 26 Mar 2021 14:09:56 GMT  
		Size: 542.5 KB (542478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33dd7c7d8f19e1deae02f062ba1b15600fcb4b6a7771735468b045db8b7f22d`  
		Last Modified: Fri, 26 Mar 2021 14:09:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06041a4fb368aa52f73f9442c3e8f71b24753304224cb647a51f50965c03f3`  
		Last Modified: Fri, 26 Mar 2021 14:09:55 GMT  
		Size: 6.9 KB (6898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93e71c8b7ad210630760ecc29f30d2891effef120e67c6a938b7d41cf9c6575`  
		Last Modified: Fri, 26 Mar 2021 14:10:06 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fcc12969517e7f7e909b5dbf5b31ab0ec31423ede1fd3787a0989d7e7779ae`  
		Last Modified: Fri, 26 Mar 2021 14:09:55 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11` - linux; ppc64le

```console
$ docker pull bonita@sha256:446e9eba83d700264d6dd2ee84ab43ebe2fd09d2f047d5e477cac804bc10e70a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231512145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18cf3c71881f7f7e5afd0e47e56f220351dcb70be31eb1c92f6d324d659c1f9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:54:50 GMT
ADD file:16a7a25947f319127d6b6ca6c99ff4e36bc4112c64ed67d2678b949eea2ad7e9 in / 
# Thu, 25 Mar 2021 22:56:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:59:22 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 16:57:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 17:00:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:01:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 17:01:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 17:01:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 17:01:47 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 17:01:55 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 17:02:02 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 17:02:12 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 17:02:17 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 26 Mar 2021 17:02:26 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 26 Mar 2021 17:02:38 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 17:02:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 17:02:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 17:03:11 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 17:03:28 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 17:03:36 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 26 Mar 2021 17:03:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 26 Mar 2021 17:04:10 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 17:04:24 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 17:04:29 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 17:04:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 17:04:38 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 17:04:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:5ade347cf74df0ad62b82c57b0a6f0411ef9ecad9336a99c9e116ee5d1ff3d82`  
		Last Modified: Thu, 25 Mar 2021 23:15:40 GMT  
		Size: 30.4 MB (30423262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918394a3ae216a0c5018f2cb9895614a0b9689fca3efc24700f5e1b1866273ad`  
		Last Modified: Thu, 25 Mar 2021 23:15:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dcfbdd713e2165e8011c88e37ddcbc43523f8f06ee41b65fa9edf100f0cebc`  
		Last Modified: Fri, 26 Mar 2021 17:08:55 GMT  
		Size: 87.2 MB (87187374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7279cfc51feea32c6ce6ff6a7154c575e7d99a4fa22398ed8ec8a463e63c656b`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdde82b9d378f4b5dbc93460991eef8e85aa8fb50a6ac82dc50241dcf3324538`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dace4db6d23b69db02a954695ce320a7335cf6ef057d6d7bbd09123f56acda`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 541.8 KB (541849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1478ae9dfa1b4a241085a53772a716b6091f03c29679a14ea049734d123e49c`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7a77f393a8ab07a80aeaa829e1f17e3a10001bf81b4dabe8626fd40130a0bc`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 6.9 KB (6890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf170323d26fa773a9177cffb234aaa17e28634f39d1da39b3296558c8bdd26`  
		Last Modified: Fri, 26 Mar 2021 17:08:45 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32e36cc0af4374922e7292f5640a266c81c0ba98f20cd6f7cc5a1c33e6e9bba`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.11.4`

```console
$ docker pull bonita@sha256:bea03469bae4d92ca9a760d5ad452fbb4b7cb74393979e0b29f6e09b6ab62337
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.11.4` - linux; amd64

```console
$ docker pull bonita@sha256:b694e19ef9ac650a23887d2c22c36276b9f48993eed040886e30b147c9b88ea8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.8 MB (235826347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd1d641447e311f7e0cd7a0dd4672a56e5d7c6d2a49334a909ee29f9f41cf6fd`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:54:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 09:54:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:54:35 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 09:54:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 09:54:38 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 09:54:39 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 26 Mar 2021 09:54:39 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 26 Mar 2021 09:54:39 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 09:54:39 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 09:54:39 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 09:54:40 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 09:54:41 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 09:54:41 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 26 Mar 2021 09:54:47 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 26 Mar 2021 09:54:49 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 09:54:51 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 09:54:51 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 09:54:51 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 09:54:51 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 09:54:51 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e534248c77c94586396089f5fe1e6ef3445619f3b25b01e3788c31a39246de`  
		Last Modified: Fri, 26 Mar 2021 09:56:17 GMT  
		Size: 95.2 MB (95182928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51fffa5c2969e00e61b80759c01c7b29a445487471b69cab746c2912685b51`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0795bb218aad676992e4855a54a7a8fbf0139bdb13b12a54e94c512da7714`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef20992b153c738c647dc0b493b155dc50a750365be70fcf88cfe88ce28b63d`  
		Last Modified: Fri, 26 Mar 2021 09:56:00 GMT  
		Size: 573.0 KB (572988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2342ed4cdb3bb862f5ee7bebbc9876f88377e7143203e1d9356aa2ad597373dc`  
		Last Modified: Fri, 26 Mar 2021 09:55:59 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8ade80e567ac70f7da85f2303331a1637cb679e23c1c02fcd30ad8b60fc5ea`  
		Last Modified: Fri, 26 Mar 2021 09:55:59 GMT  
		Size: 6.9 KB (6891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e4b5d9808791fa19090b61806ed17ea0c9fdc6a9d0f96f815830d9fe297251`  
		Last Modified: Fri, 26 Mar 2021 09:56:05 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfb68eeef2f54c5a0c542b65ba7fc90440c48b38740396b882c0e8d356613cb`  
		Last Modified: Fri, 26 Mar 2021 09:55:59 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:595db97e2cf776906c9ddce8d546636495feefcad54433725011a05e0dff57c2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.9 MB (223906185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac3ea304f138a40bf1efa2960c4dc1fc106e954dd178a5bf2af20463bc846a5`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:06:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 14:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:07:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 14:07:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 14:07:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 14:07:24 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 14:07:25 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 14:07:26 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 14:07:28 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 14:07:30 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 26 Mar 2021 14:07:31 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 26 Mar 2021 14:07:33 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 14:07:34 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 14:07:36 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 14:07:41 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 14:07:45 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 14:07:47 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 26 Mar 2021 14:07:55 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 26 Mar 2021 14:07:59 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 14:08:03 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 14:08:04 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 14:08:06 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 14:08:08 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 14:08:09 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5c85b2acaf4dee357935720ab250421d16571fef3e471780b122f2cdf83af`  
		Last Modified: Fri, 26 Mar 2021 14:10:17 GMT  
		Size: 86.3 MB (86271251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c2fdd692d74aaecc195ddf2db73f8559e338bead6fea0723ebf300f960e59`  
		Last Modified: Fri, 26 Mar 2021 14:09:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bcf42f29aedf6bbe85cc51f150084420ac531553a9612c2f879ee3bd0078f`  
		Last Modified: Fri, 26 Mar 2021 14:09:57 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e49ab418707059be0c1d66745b5321be3a596a356b98745231078ea5c4a0f98`  
		Last Modified: Fri, 26 Mar 2021 14:09:56 GMT  
		Size: 542.5 KB (542478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c33dd7c7d8f19e1deae02f062ba1b15600fcb4b6a7771735468b045db8b7f22d`  
		Last Modified: Fri, 26 Mar 2021 14:09:55 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a06041a4fb368aa52f73f9442c3e8f71b24753304224cb647a51f50965c03f3`  
		Last Modified: Fri, 26 Mar 2021 14:09:55 GMT  
		Size: 6.9 KB (6898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93e71c8b7ad210630760ecc29f30d2891effef120e67c6a938b7d41cf9c6575`  
		Last Modified: Fri, 26 Mar 2021 14:10:06 GMT  
		Size: 113.3 MB (113347828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fcc12969517e7f7e909b5dbf5b31ab0ec31423ede1fd3787a0989d7e7779ae`  
		Last Modified: Fri, 26 Mar 2021 14:09:55 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.11.4` - linux; ppc64le

```console
$ docker pull bonita@sha256:446e9eba83d700264d6dd2ee84ab43ebe2fd09d2f047d5e477cac804bc10e70a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.5 MB (231512145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d18cf3c71881f7f7e5afd0e47e56f220351dcb70be31eb1c92f6d324d659c1f9`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:54:50 GMT
ADD file:16a7a25947f319127d6b6ca6c99ff4e36bc4112c64ed67d2678b949eea2ad7e9 in / 
# Thu, 25 Mar 2021 22:56:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:59:22 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 16:57:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 17:00:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:01:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 17:01:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 17:01:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 17:01:47 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 17:01:55 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 17:02:02 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 17:02:12 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 17:02:17 GMT
ENV BONITA_VERSION=7.11.4
# Fri, 26 Mar 2021 17:02:26 GMT
ENV BONITA_SHA256=5366b61bd36567b1fc62e8cb1d40a78a613c18c0d6eb894e9c414f57269b7d18
# Fri, 26 Mar 2021 17:02:38 GMT
ENV ZIP_FILE=BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 17:02:42 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 17:02:47 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/7.11.4/BonitaCommunity-7.11.4.zip
# Fri, 26 Mar 2021 17:03:11 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 17:03:28 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 17:03:36 GMT
COPY dir:224f3f698a7c2ba0960fd1c61d1b42d86ab0dee604621557635c99e6a0a6ec2d in /opt/files 
# Fri, 26 Mar 2021 17:03:54 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BONITA_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BONITA_VERSION}.zip; fi
# Fri, 26 Mar 2021 17:04:10 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 17:04:24 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 17:04:29 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 17:04:32 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 17:04:38 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 17:04:45 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:5ade347cf74df0ad62b82c57b0a6f0411ef9ecad9336a99c9e116ee5d1ff3d82`  
		Last Modified: Thu, 25 Mar 2021 23:15:40 GMT  
		Size: 30.4 MB (30423262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918394a3ae216a0c5018f2cb9895614a0b9689fca3efc24700f5e1b1866273ad`  
		Last Modified: Thu, 25 Mar 2021 23:15:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dcfbdd713e2165e8011c88e37ddcbc43523f8f06ee41b65fa9edf100f0cebc`  
		Last Modified: Fri, 26 Mar 2021 17:08:55 GMT  
		Size: 87.2 MB (87187374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7279cfc51feea32c6ce6ff6a7154c575e7d99a4fa22398ed8ec8a463e63c656b`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdde82b9d378f4b5dbc93460991eef8e85aa8fb50a6ac82dc50241dcf3324538`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dace4db6d23b69db02a954695ce320a7335cf6ef057d6d7bbd09123f56acda`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 541.8 KB (541849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1478ae9dfa1b4a241085a53772a716b6091f03c29679a14ea049734d123e49c`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e7a77f393a8ab07a80aeaa829e1f17e3a10001bf81b4dabe8626fd40130a0bc`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 6.9 KB (6890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbf170323d26fa773a9177cffb234aaa17e28634f39d1da39b3296558c8bdd26`  
		Last Modified: Fri, 26 Mar 2021 17:08:45 GMT  
		Size: 113.3 MB (113347830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e32e36cc0af4374922e7292f5640a266c81c0ba98f20cd6f7cc5a1c33e6e9bba`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 1.7 KB (1711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12`

```console
$ docker pull bonita@sha256:1bb3971e7fb1b18c92b6b0bada9c8b3df0b392051789b9062f1907e39892ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12` - linux; amd64

```console
$ docker pull bonita@sha256:bec7c62bfa26447c37ea9a71f638671f52400db14f9229eeee8e7df6a6a299b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238893974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce2c8eced3ba09353d4f974632f31ecce2489fc06865b589740531b2abbd1d3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:54:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 09:54:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:54:35 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 09:54:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 09:54:38 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 09:54:57 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 09:54:57 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 09:54:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 09:54:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 09:54:59 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 09:55:00 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 09:55:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 09:55:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 09:55:07 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 09:55:09 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 09:55:09 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 09:55:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 09:55:09 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 09:55:09 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e534248c77c94586396089f5fe1e6ef3445619f3b25b01e3788c31a39246de`  
		Last Modified: Fri, 26 Mar 2021 09:56:17 GMT  
		Size: 95.2 MB (95182928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51fffa5c2969e00e61b80759c01c7b29a445487471b69cab746c2912685b51`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0795bb218aad676992e4855a54a7a8fbf0139bdb13b12a54e94c512da7714`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef20992b153c738c647dc0b493b155dc50a750365be70fcf88cfe88ce28b63d`  
		Last Modified: Fri, 26 Mar 2021 09:56:00 GMT  
		Size: 573.0 KB (572988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab13c0cfd407a99af4475a201b0e82ef59eb70270e887c1d76519a390f6df46`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fef7e4f41959abb0200ce52dbf1df79a3a1c6e2135817fa0b950601145d24a`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa40d92e0791bad639df8e2c95739cc01e6fc08a1c47bac8675668516852dba`  
		Last Modified: Fri, 26 Mar 2021 09:56:37 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4dbd4b7563e31dcb93c41f4ddce6c2216761188046dc480a97cd1199207e72`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:84030597fea55c49a48a9eed24ac7eda2edb032d525d4cf0ccd9d04abc1149a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226973813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821bd2f3d2ce3bc73a3dcf96a4de7947e6474c1ea9878f60436f6cbf347e71ac`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:06:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 14:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:07:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 14:07:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 14:07:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 14:07:24 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 14:08:18 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 14:08:19 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 14:08:20 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 14:08:21 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 14:08:21 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 14:08:22 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 14:08:23 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 14:08:24 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 14:08:25 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 14:08:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 14:08:34 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 14:08:36 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 14:08:37 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 14:08:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 14:08:46 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 14:08:51 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 14:08:52 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 14:08:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 14:08:56 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 14:08:57 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5c85b2acaf4dee357935720ab250421d16571fef3e471780b122f2cdf83af`  
		Last Modified: Fri, 26 Mar 2021 14:10:17 GMT  
		Size: 86.3 MB (86271251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c2fdd692d74aaecc195ddf2db73f8559e338bead6fea0723ebf300f960e59`  
		Last Modified: Fri, 26 Mar 2021 14:09:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bcf42f29aedf6bbe85cc51f150084420ac531553a9612c2f879ee3bd0078f`  
		Last Modified: Fri, 26 Mar 2021 14:09:57 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e49ab418707059be0c1d66745b5321be3a596a356b98745231078ea5c4a0f98`  
		Last Modified: Fri, 26 Mar 2021 14:09:56 GMT  
		Size: 542.5 KB (542478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa07e9e63eacc299ff02c8c939a04a38e581f5885ed74953fa8dcbd9a11e27`  
		Last Modified: Fri, 26 Mar 2021 14:10:26 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03afcbb1b94d8b23243e19af274991ce7d143eec99fc30a3b905d442cd576aaa`  
		Last Modified: Fri, 26 Mar 2021 14:10:25 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae05ebc2888a5b8cd66f45562ad4677e9b984afc66311d568431230557f8f1b4`  
		Last Modified: Fri, 26 Mar 2021 14:10:37 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cee0632a7f0f0e126c55e70fab96fa8540c079acd2d96380460c09dc2705374`  
		Last Modified: Fri, 26 Mar 2021 14:10:25 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12` - linux; ppc64le

```console
$ docker pull bonita@sha256:b212334198bfe535cb9fa6a435e38796b9a47a4a043346a23bd772588b3f9488
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234579781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d51c75ce92943c2cbd2bf2cfa58b039d33b7c95022893f681a1677e52866bef`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:54:50 GMT
ADD file:16a7a25947f319127d6b6ca6c99ff4e36bc4112c64ed67d2678b949eea2ad7e9 in / 
# Thu, 25 Mar 2021 22:56:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:59:22 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 16:57:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 17:00:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:01:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 17:01:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 17:01:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 17:01:47 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 17:05:04 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 17:05:13 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 17:05:20 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 17:05:22 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 17:05:29 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 17:05:32 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 17:05:38 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 17:05:45 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 17:05:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 17:05:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 17:06:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 17:06:16 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 17:06:18 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 17:06:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 17:06:48 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 17:07:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 17:07:06 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 17:07:08 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 17:07:14 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 17:07:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:5ade347cf74df0ad62b82c57b0a6f0411ef9ecad9336a99c9e116ee5d1ff3d82`  
		Last Modified: Thu, 25 Mar 2021 23:15:40 GMT  
		Size: 30.4 MB (30423262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918394a3ae216a0c5018f2cb9895614a0b9689fca3efc24700f5e1b1866273ad`  
		Last Modified: Thu, 25 Mar 2021 23:15:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dcfbdd713e2165e8011c88e37ddcbc43523f8f06ee41b65fa9edf100f0cebc`  
		Last Modified: Fri, 26 Mar 2021 17:08:55 GMT  
		Size: 87.2 MB (87187374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7279cfc51feea32c6ce6ff6a7154c575e7d99a4fa22398ed8ec8a463e63c656b`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdde82b9d378f4b5dbc93460991eef8e85aa8fb50a6ac82dc50241dcf3324538`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dace4db6d23b69db02a954695ce320a7335cf6ef057d6d7bbd09123f56acda`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 541.8 KB (541849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107b99fec4b745157230b018539d14317dbf688634bab8a5c5b96c6c9da5206`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfd93428c77e1a39586ba0191b041dee349e2c444aaa68bab9b0eccbb62ae0`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332474a1847cac1f6d92aff976376e8781b200ea908f7e4bf41159e720c03202`  
		Last Modified: Fri, 26 Mar 2021 17:09:18 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0660aed029edb19c64bdb515578304dc1c653850bd654b97072f9db68a8c2bf`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:7.12.1`

```console
$ docker pull bonita@sha256:1bb3971e7fb1b18c92b6b0bada9c8b3df0b392051789b9062f1907e39892ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:7.12.1` - linux; amd64

```console
$ docker pull bonita@sha256:bec7c62bfa26447c37ea9a71f638671f52400db14f9229eeee8e7df6a6a299b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238893974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce2c8eced3ba09353d4f974632f31ecce2489fc06865b589740531b2abbd1d3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:54:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 09:54:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:54:35 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 09:54:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 09:54:38 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 09:54:57 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 09:54:57 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 09:54:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 09:54:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 09:54:59 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 09:55:00 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 09:55:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 09:55:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 09:55:07 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 09:55:09 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 09:55:09 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 09:55:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 09:55:09 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 09:55:09 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e534248c77c94586396089f5fe1e6ef3445619f3b25b01e3788c31a39246de`  
		Last Modified: Fri, 26 Mar 2021 09:56:17 GMT  
		Size: 95.2 MB (95182928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51fffa5c2969e00e61b80759c01c7b29a445487471b69cab746c2912685b51`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0795bb218aad676992e4855a54a7a8fbf0139bdb13b12a54e94c512da7714`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef20992b153c738c647dc0b493b155dc50a750365be70fcf88cfe88ce28b63d`  
		Last Modified: Fri, 26 Mar 2021 09:56:00 GMT  
		Size: 573.0 KB (572988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab13c0cfd407a99af4475a201b0e82ef59eb70270e887c1d76519a390f6df46`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fef7e4f41959abb0200ce52dbf1df79a3a1c6e2135817fa0b950601145d24a`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa40d92e0791bad639df8e2c95739cc01e6fc08a1c47bac8675668516852dba`  
		Last Modified: Fri, 26 Mar 2021 09:56:37 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4dbd4b7563e31dcb93c41f4ddce6c2216761188046dc480a97cd1199207e72`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:84030597fea55c49a48a9eed24ac7eda2edb032d525d4cf0ccd9d04abc1149a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226973813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821bd2f3d2ce3bc73a3dcf96a4de7947e6474c1ea9878f60436f6cbf347e71ac`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:06:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 14:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:07:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 14:07:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 14:07:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 14:07:24 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 14:08:18 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 14:08:19 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 14:08:20 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 14:08:21 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 14:08:21 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 14:08:22 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 14:08:23 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 14:08:24 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 14:08:25 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 14:08:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 14:08:34 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 14:08:36 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 14:08:37 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 14:08:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 14:08:46 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 14:08:51 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 14:08:52 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 14:08:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 14:08:56 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 14:08:57 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5c85b2acaf4dee357935720ab250421d16571fef3e471780b122f2cdf83af`  
		Last Modified: Fri, 26 Mar 2021 14:10:17 GMT  
		Size: 86.3 MB (86271251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c2fdd692d74aaecc195ddf2db73f8559e338bead6fea0723ebf300f960e59`  
		Last Modified: Fri, 26 Mar 2021 14:09:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bcf42f29aedf6bbe85cc51f150084420ac531553a9612c2f879ee3bd0078f`  
		Last Modified: Fri, 26 Mar 2021 14:09:57 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e49ab418707059be0c1d66745b5321be3a596a356b98745231078ea5c4a0f98`  
		Last Modified: Fri, 26 Mar 2021 14:09:56 GMT  
		Size: 542.5 KB (542478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa07e9e63eacc299ff02c8c939a04a38e581f5885ed74953fa8dcbd9a11e27`  
		Last Modified: Fri, 26 Mar 2021 14:10:26 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03afcbb1b94d8b23243e19af274991ce7d143eec99fc30a3b905d442cd576aaa`  
		Last Modified: Fri, 26 Mar 2021 14:10:25 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae05ebc2888a5b8cd66f45562ad4677e9b984afc66311d568431230557f8f1b4`  
		Last Modified: Fri, 26 Mar 2021 14:10:37 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cee0632a7f0f0e126c55e70fab96fa8540c079acd2d96380460c09dc2705374`  
		Last Modified: Fri, 26 Mar 2021 14:10:25 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:7.12.1` - linux; ppc64le

```console
$ docker pull bonita@sha256:b212334198bfe535cb9fa6a435e38796b9a47a4a043346a23bd772588b3f9488
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234579781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d51c75ce92943c2cbd2bf2cfa58b039d33b7c95022893f681a1677e52866bef`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:54:50 GMT
ADD file:16a7a25947f319127d6b6ca6c99ff4e36bc4112c64ed67d2678b949eea2ad7e9 in / 
# Thu, 25 Mar 2021 22:56:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:59:22 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 16:57:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 17:00:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:01:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 17:01:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 17:01:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 17:01:47 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 17:05:04 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 17:05:13 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 17:05:20 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 17:05:22 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 17:05:29 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 17:05:32 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 17:05:38 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 17:05:45 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 17:05:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 17:05:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 17:06:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 17:06:16 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 17:06:18 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 17:06:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 17:06:48 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 17:07:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 17:07:06 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 17:07:08 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 17:07:14 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 17:07:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:5ade347cf74df0ad62b82c57b0a6f0411ef9ecad9336a99c9e116ee5d1ff3d82`  
		Last Modified: Thu, 25 Mar 2021 23:15:40 GMT  
		Size: 30.4 MB (30423262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918394a3ae216a0c5018f2cb9895614a0b9689fca3efc24700f5e1b1866273ad`  
		Last Modified: Thu, 25 Mar 2021 23:15:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dcfbdd713e2165e8011c88e37ddcbc43523f8f06ee41b65fa9edf100f0cebc`  
		Last Modified: Fri, 26 Mar 2021 17:08:55 GMT  
		Size: 87.2 MB (87187374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7279cfc51feea32c6ce6ff6a7154c575e7d99a4fa22398ed8ec8a463e63c656b`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdde82b9d378f4b5dbc93460991eef8e85aa8fb50a6ac82dc50241dcf3324538`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dace4db6d23b69db02a954695ce320a7335cf6ef057d6d7bbd09123f56acda`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 541.8 KB (541849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107b99fec4b745157230b018539d14317dbf688634bab8a5c5b96c6c9da5206`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfd93428c77e1a39586ba0191b041dee349e2c444aaa68bab9b0eccbb62ae0`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332474a1847cac1f6d92aff976376e8781b200ea908f7e4bf41159e720c03202`  
		Last Modified: Fri, 26 Mar 2021 17:09:18 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0660aed029edb19c64bdb515578304dc1c653850bd654b97072f9db68a8c2bf`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `bonita:latest`

```console
$ docker pull bonita@sha256:1bb3971e7fb1b18c92b6b0bada9c8b3df0b392051789b9062f1907e39892ad6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `bonita:latest` - linux; amd64

```console
$ docker pull bonita@sha256:bec7c62bfa26447c37ea9a71f638671f52400db14f9229eeee8e7df6a6a299b5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.9 MB (238893974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce2c8eced3ba09353d4f974632f31ecce2489fc06865b589740531b2abbd1d3`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:32:58 GMT
ADD file:e80ae8d359b484dac5346f98c549abc694e1d0c87e1d9753d495aed4d9c8b2b3 in / 
# Thu, 25 Mar 2021 22:32:59 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:33:00 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:33:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:33:02 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 09:54:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 09:54:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:54:35 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 09:54:36 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 09:54:38 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 09:54:38 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 09:54:56 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 09:54:57 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 09:54:57 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 09:54:57 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 09:54:58 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 09:54:58 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 09:54:59 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 09:55:00 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 09:55:00 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 09:55:05 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 09:55:07 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 09:55:09 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 09:55:09 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 09:55:09 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 09:55:09 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 09:55:09 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:6e0aa5e7af40303f56126b1469d1f37525b3a55a788836a6c9b773f6ce8bc446`  
		Last Modified: Thu, 25 Mar 2021 22:34:24 GMT  
		Size: 26.7 MB (26710781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47239a868b3375462d644f2ffb1b20114623fac03109d2950bdf0d57ab487d2`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49cbb10cca8504e3dbd65eb5db3c1dd0cd27070154386f819c5936de321c14b1`  
		Last Modified: Thu, 25 Mar 2021 22:34:20 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e534248c77c94586396089f5fe1e6ef3445619f3b25b01e3788c31a39246de`  
		Last Modified: Fri, 26 Mar 2021 09:56:17 GMT  
		Size: 95.2 MB (95182928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab51fffa5c2969e00e61b80759c01c7b29a445487471b69cab746c2912685b51`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ca0795bb218aad676992e4855a54a7a8fbf0139bdb13b12a54e94c512da7714`  
		Last Modified: Fri, 26 Mar 2021 09:56:02 GMT  
		Size: 1.9 KB (1878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bef20992b153c738c647dc0b493b155dc50a750365be70fcf88cfe88ce28b63d`  
		Last Modified: Fri, 26 Mar 2021 09:56:00 GMT  
		Size: 573.0 KB (572988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab13c0cfd407a99af4475a201b0e82ef59eb70270e887c1d76519a390f6df46`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01fef7e4f41959abb0200ce52dbf1df79a3a1c6e2135817fa0b950601145d24a`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 6.9 KB (6946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa40d92e0791bad639df8e2c95739cc01e6fc08a1c47bac8675668516852dba`  
		Last Modified: Fri, 26 Mar 2021 09:56:37 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4dbd4b7563e31dcb93c41f4ddce6c2216761188046dc480a97cd1199207e72`  
		Last Modified: Fri, 26 Mar 2021 09:56:29 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; arm64 variant v8

```console
$ docker pull bonita@sha256:84030597fea55c49a48a9eed24ac7eda2edb032d525d4cf0ccd9d04abc1149a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (226973813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:821bd2f3d2ce3bc73a3dcf96a4de7947e6474c1ea9878f60436f6cbf347e71ac`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 23:21:42 GMT
ADD file:c2ebeb57ae78696b3c16020bf2c3030d8f36acd3032907fea3fec885ac614541 in / 
# Thu, 25 Mar 2021 23:21:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 23:21:57 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 23:22:01 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 23:22:07 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 14:06:14 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 14:07:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 14:07:17 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 14:07:19 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 14:07:23 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 14:07:24 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 14:08:18 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 14:08:19 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 14:08:20 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 14:08:21 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 14:08:21 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 14:08:22 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 14:08:23 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 14:08:24 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 14:08:25 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 14:08:26 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 14:08:34 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 14:08:36 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 14:08:37 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 14:08:42 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 14:08:46 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 14:08:51 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 14:08:52 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 14:08:53 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 14:08:56 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 14:08:57 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:af9ca2923c1e73640f6df497fc7fc63e3c2e24892f1d6abbd4225542339b6e06`  
		Last Modified: Thu, 25 Mar 2021 23:27:04 GMT  
		Size: 23.7 MB (23732791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2babfbd9d095d8a0dc7cfbaa658447a483120087d4ea77cae9ee9a78e370c2`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83b7f31d752fef6bce03359dc68487e2d02040b70c57526b72004a0ced4cbf5`  
		Last Modified: Thu, 25 Mar 2021 23:26:58 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa5c85b2acaf4dee357935720ab250421d16571fef3e471780b122f2cdf83af`  
		Last Modified: Fri, 26 Mar 2021 14:10:17 GMT  
		Size: 86.3 MB (86271251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653c2fdd692d74aaecc195ddf2db73f8559e338bead6fea0723ebf300f960e59`  
		Last Modified: Fri, 26 Mar 2021 14:09:59 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288bcf42f29aedf6bbe85cc51f150084420ac531553a9612c2f879ee3bd0078f`  
		Last Modified: Fri, 26 Mar 2021 14:09:57 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e49ab418707059be0c1d66745b5321be3a596a356b98745231078ea5c4a0f98`  
		Last Modified: Fri, 26 Mar 2021 14:09:56 GMT  
		Size: 542.5 KB (542478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fa07e9e63eacc299ff02c8c939a04a38e581f5885ed74953fa8dcbd9a11e27`  
		Last Modified: Fri, 26 Mar 2021 14:10:26 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03afcbb1b94d8b23243e19af274991ce7d143eec99fc30a3b905d442cd576aaa`  
		Last Modified: Fri, 26 Mar 2021 14:10:25 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae05ebc2888a5b8cd66f45562ad4677e9b984afc66311d568431230557f8f1b4`  
		Last Modified: Fri, 26 Mar 2021 14:10:37 GMT  
		Size: 116.4 MB (116415405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cee0632a7f0f0e126c55e70fab96fa8540c079acd2d96380460c09dc2705374`  
		Last Modified: Fri, 26 Mar 2021 14:10:25 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `bonita:latest` - linux; ppc64le

```console
$ docker pull bonita@sha256:b212334198bfe535cb9fa6a435e38796b9a47a4a043346a23bd772588b3f9488
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234579781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d51c75ce92943c2cbd2bf2cfa58b039d33b7c95022893f681a1677e52866bef`
-	Default Command: `["\/opt\/files\/startup.sh"]`

```dockerfile
# Thu, 25 Mar 2021 22:54:50 GMT
ADD file:16a7a25947f319127d6b6ca6c99ff4e36bc4112c64ed67d2678b949eea2ad7e9 in / 
# Thu, 25 Mar 2021 22:56:08 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Thu, 25 Mar 2021 22:57:02 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Thu, 25 Mar 2021 22:57:52 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Thu, 25 Mar 2021 22:59:22 GMT
CMD ["/bin/bash"]
# Fri, 26 Mar 2021 16:57:02 GMT
LABEL maintainer=Bonitasoft Runtime team <rd.engine@bonitasoft.com>
# Fri, 26 Mar 2021 17:00:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends   curl   gnupg2   mysql-client-core-5.7   openjdk-11-jre-headless   postgresql-client   unzip   zip   && rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:01:08 GMT
RUN mkdir /opt/custom-init.d/
# Fri, 26 Mar 2021 17:01:21 GMT
RUN groupadd -r bonita -g 1000   && useradd -u 1000 -r -g bonita -d /opt/bonita/ -s /sbin/nologin -c "Bonita User" bonita
# Fri, 26 Mar 2021 17:01:41 GMT
RUN (gpg --keyserver ha.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4   || gpg --keyserver ipv4.pool.sks-keyservers.net --recv-keys B42F6819007F00F88E364FD4036A9C25BF357DD4)   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture)" -o /usr/local/bin/gosu   && curl -fsSL "https://github.com/tianon/gosu/releases/download/1.10/gosu-$(dpkg --print-architecture).asc" -o /usr/local/bin/gosu.asc   && gpg --batch --verify /usr/local/bin/gosu.asc /usr/local/bin/gosu   && rm /usr/local/bin/gosu.asc   && chmod +x /usr/local/bin/gosu
# Fri, 26 Mar 2021 17:01:47 GMT
ARG BONITA_VERSION
# Fri, 26 Mar 2021 17:05:04 GMT
ARG BRANDING_VERSION
# Fri, 26 Mar 2021 17:05:13 GMT
ARG BONITA_SHA256
# Fri, 26 Mar 2021 17:05:20 GMT
ARG BASE_URL
# Fri, 26 Mar 2021 17:05:22 GMT
ARG BONITA_URL
# Fri, 26 Mar 2021 17:05:29 GMT
ENV BONITA_VERSION=7.12.1
# Fri, 26 Mar 2021 17:05:32 GMT
ENV BRANDING_VERSION=2021.1
# Fri, 26 Mar 2021 17:05:38 GMT
ENV BONITA_SHA256=5342b18dd7f93bd3b2b64f8587504d0bf324f4f84d4259191b7291ee8f9ec693
# Fri, 26 Mar 2021 17:05:45 GMT
ENV ZIP_FILE=BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 17:05:52 GMT
ENV BASE_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download
# Fri, 26 Mar 2021 17:05:56 GMT
ENV BONITA_URL=https://github.com/bonitasoft/bonita-platform-releases/releases/download/2021.1/BonitaCommunity-2021.1.zip
# Fri, 26 Mar 2021 17:06:06 GMT
RUN echo "Downloading Bonita from url: ${BONITA_URL}"
# Fri, 26 Mar 2021 17:06:16 GMT
RUN mkdir /opt/files
# Fri, 26 Mar 2021 17:06:18 GMT
COPY dir:ceba4393fbbad2e791e9b0a75d4a81330c328bd9f67f35ff002adea48d26a677 in /opt/files 
# Fri, 26 Mar 2021 17:06:34 GMT
RUN if [ -f "/opt/files/BonitaCommunity-${BRANDING_VERSION}.zip" ]; then echo "File already present in /opt/files"; else curl -fsSL ${BONITA_URL} -o /opt/files/BonitaCommunity-${BRANDING_VERSION}.zip; fi
# Fri, 26 Mar 2021 17:06:48 GMT
RUN sha256sum /opt/files/${ZIP_FILE}
# Fri, 26 Mar 2021 17:07:01 GMT
RUN echo "$BONITA_SHA256" /opt/files/${ZIP_FILE} | sha256sum -c -
# Fri, 26 Mar 2021 17:07:06 GMT
VOLUME [/opt/bonita]
# Fri, 26 Mar 2021 17:07:08 GMT
COPY dir:c3e962ef70138930cdc6c114f07b10cd87f0a7897e828b1cf0f64aa4e7f29ecb in /opt/templates 
# Fri, 26 Mar 2021 17:07:14 GMT
EXPOSE 8080
# Fri, 26 Mar 2021 17:07:25 GMT
CMD ["/opt/files/startup.sh"]
```

-	Layers:
	-	`sha256:5ade347cf74df0ad62b82c57b0a6f0411ef9ecad9336a99c9e116ee5d1ff3d82`  
		Last Modified: Thu, 25 Mar 2021 23:15:40 GMT  
		Size: 30.4 MB (30423262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918394a3ae216a0c5018f2cb9895614a0b9689fca3efc24700f5e1b1866273ad`  
		Last Modified: Thu, 25 Mar 2021 23:15:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5795a499c24598e294527992a703053ab615879af048f3b809a3ad86141684d`  
		Last Modified: Thu, 25 Mar 2021 22:58:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47dcfbdd713e2165e8011c88e37ddcbc43523f8f06ee41b65fa9edf100f0cebc`  
		Last Modified: Fri, 26 Mar 2021 17:08:55 GMT  
		Size: 87.2 MB (87187374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7279cfc51feea32c6ce6ff6a7154c575e7d99a4fa22398ed8ec8a463e63c656b`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdde82b9d378f4b5dbc93460991eef8e85aa8fb50a6ac82dc50241dcf3324538`  
		Last Modified: Fri, 26 Mar 2021 17:08:39 GMT  
		Size: 1.9 KB (1887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dace4db6d23b69db02a954695ce320a7335cf6ef057d6d7bbd09123f56acda`  
		Last Modified: Fri, 26 Mar 2021 17:08:35 GMT  
		Size: 541.8 KB (541849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4107b99fec4b745157230b018539d14317dbf688634bab8a5c5b96c6c9da5206`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 148.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1dfd93428c77e1a39586ba0191b041dee349e2c444aaa68bab9b0eccbb62ae0`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 6.9 KB (6947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332474a1847cac1f6d92aff976376e8781b200ea908f7e4bf41159e720c03202`  
		Last Modified: Fri, 26 Mar 2021 17:09:18 GMT  
		Size: 116.4 MB (116415408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0660aed029edb19c64bdb515578304dc1c653850bd654b97072f9db68a8c2bf`  
		Last Modified: Fri, 26 Mar 2021 17:09:07 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
