<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.2.3-b1`](#silverpeas623-b1)
-	[`silverpeas:6.3.3`](#silverpeas633)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.2.3-b1`

```console
$ docker pull silverpeas@sha256:01dd93fb66159ef1c7ccc16c9b177de81741d54bc4979c05200dfb43232df0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.2.3-b1` - linux; amd64

```console
$ docker pull silverpeas@sha256:0f3089d7a112636a0f47f76454b4e2c4a64381412a1d88a16f8cca272386aa5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1749441878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18da163472a81e7859077ca6f1b898b3822a244826b2256260cef18b4b3b44a3`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Wed, 13 Dec 2023 10:27:43 GMT
ARG RELEASE
# Wed, 13 Dec 2023 10:27:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 13 Dec 2023 10:27:44 GMT
LABEL org.opencontainers.image.version=20.04
# Wed, 13 Dec 2023 10:27:45 GMT
ADD file:5696198fbfd4074852bdee76ffd84da75da8de76727cef4f0cdd265f7bee6b76 in / 
# Wed, 13 Dec 2023 10:27:45 GMT
CMD ["/bin/bash"]
# Sat, 16 Dec 2023 13:00:31 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Sat, 16 Dec 2023 13:00:31 GMT
ENV TERM=xterm
# Sat, 16 Dec 2023 13:06:32 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Sat, 16 Dec 2023 13:07:52 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Sat, 16 Dec 2023 13:07:56 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Sat, 16 Dec 2023 13:07:56 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Sat, 16 Dec 2023 13:08:34 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Sat, 16 Dec 2023 13:08:34 GMT
ENV LANG=en_US.UTF-8
# Sat, 16 Dec 2023 13:08:35 GMT
ENV LANGUAGE=en_US.UTF-8
# Sat, 16 Dec 2023 13:08:35 GMT
ENV LC_ALL=en_US.UTF-8
# Sat, 16 Dec 2023 13:08:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Sat, 16 Dec 2023 13:08:36 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Sat, 16 Dec 2023 13:08:36 GMT
ENV JAVA_HOME=/docker-java-home
# Sat, 16 Dec 2023 13:08:36 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Sat, 16 Dec 2023 13:08:36 GMT
ENV JBOSS_HOME=/opt/wildfly
# Sat, 16 Dec 2023 13:11:55 GMT
ENV SILVERPEAS_VERSION=6.2.3
# Sat, 16 Dec 2023 13:11:55 GMT
ENV WILDFLY_VERSION=20.0.1
# Sat, 16 Dec 2023 13:11:55 GMT
LABEL name=Silverpeas 6.2.3 description=Image to install and to run Silverpeas 6.2.3 vendor=Silverpeas version=6.2.3 build=2
# Sat, 16 Dec 2023 13:12:40 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Sat, 16 Dec 2023 13:12:41 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Sat, 16 Dec 2023 13:12:41 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Sat, 16 Dec 2023 13:12:41 GMT
WORKDIR /opt/silverpeas/bin
# Sat, 16 Dec 2023 13:12:41 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Sat, 16 Dec 2023 13:12:41 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Sat, 16 Dec 2023 13:14:24 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Sat, 16 Dec 2023 13:14:27 GMT
EXPOSE 8000 9990
# Sat, 16 Dec 2023 13:14:27 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Sat, 16 Dec 2023 13:14:27 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:521f275cc58bdab90307a5929f8a6d197368b8c214edbc7f06fc1aaf48cfff3e`  
		Last Modified: Wed, 13 Dec 2023 14:46:20 GMT  
		Size: 28.6 MB (28584024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4e5e2faf3dd0468c774a9aa946fbcc54ff3193f53eff6420e4456222262989`  
		Last Modified: Sat, 16 Dec 2023 13:16:03 GMT  
		Size: 762.3 MB (762332518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8511345f79fb02b951ad61dee1a4b742be9183a1a0ae10675be37699b2e62e2`  
		Last Modified: Sat, 16 Dec 2023 13:14:44 GMT  
		Size: 4.0 MB (3994077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:825a79f05685aaa70563d6bcb2d4a50c5bcf5d325fa66e647edc6ef02cd9470a`  
		Last Modified: Sat, 16 Dec 2023 13:14:44 GMT  
		Size: 7.1 MB (7146669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5eb87f76a4d2f3dcf1f1ad8ee6d9d920f373e83410c4cf1149811d908f5f2d`  
		Last Modified: Sat, 16 Dec 2023 13:14:42 GMT  
		Size: 2.5 MB (2534355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a011f392b70f85edc2d69bca49cb61bac386598ab8a96f50949b9e25da78113c`  
		Last Modified: Sat, 16 Dec 2023 13:14:41 GMT  
		Size: 241.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8847917dff9ca77badd1e68b953d7cd476f9a909f69370ddf012cd857f6a2e0`  
		Last Modified: Sat, 16 Dec 2023 13:14:41 GMT  
		Size: 131.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64af7740a99c23f319e947bbd90c873fbf178a4a0e98bd56120bb2eda5d15829`  
		Last Modified: Sat, 16 Dec 2023 13:16:26 GMT  
		Size: 196.8 MB (196774216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492fe621d3424dab7f6887b2428b060061a174a75d8348d585d34f556bcf59d7`  
		Last Modified: Sat, 16 Dec 2023 13:16:14 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1e150bd46919157daeef4897a93576e28347310bf1a750040363002de62633`  
		Last Modified: Sat, 16 Dec 2023 13:16:14 GMT  
		Size: 664.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef04e7146fd38eb2b890714067d6c847a31a41c8ef28c131bba47c164568731`  
		Last Modified: Sat, 16 Dec 2023 13:16:14 GMT  
		Size: 875.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38609d0ab22e646adb83a90861476f4ce33ac0da242412505d95c1d0c0635060`  
		Last Modified: Sat, 16 Dec 2023 13:16:14 GMT  
		Size: 385.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e427724c740718e194362a207c209eb2f7cfdfec9c238c53d6f1e05dd2a79c2b`  
		Last Modified: Sat, 16 Dec 2023 13:16:45 GMT  
		Size: 748.1 MB (748073317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:6.3.3`

```console
$ docker pull silverpeas@sha256:206a8c9041001ce65f0b8bd236e60e35e556aeab1a3d6578b814cda2b248614e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:6.3.3` - linux; amd64

```console
$ docker pull silverpeas@sha256:463020dc703b6cba3c419d12a2de01ae655745865770c5af20a748b143d36c41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1831609792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e07732c7a634ca2e1bbaceedd7a96532fda6b6f130d82f2be651e1c31d6da4`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 03:27:47 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 02 Feb 2024 03:27:47 GMT
ENV TERM=xterm
# Fri, 02 Feb 2024 03:35:45 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 02 Feb 2024 03:35:52 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 02 Feb 2024 03:35:56 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 02 Feb 2024 03:35:56 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 02 Feb 2024 03:36:34 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 02 Feb 2024 03:36:34 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 03:36:34 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 02 Feb 2024 03:36:34 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 03:36:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 02 Feb 2024 03:36:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 02 Feb 2024 03:36:35 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 02 Feb 2024 03:36:36 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 02 Feb 2024 03:36:36 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 02 Feb 2024 03:36:36 GMT
ENV SILVERPEAS_VERSION=6.3.3
# Fri, 02 Feb 2024 03:36:36 GMT
ENV WILDFLY_VERSION=26.1.1
# Fri, 02 Feb 2024 03:36:36 GMT
LABEL name=Silverpeas 6.3.3 description=Image to install and to run Silverpeas 6.3.3 vendor=Silverpeas version=6.3.3 build=1
# Fri, 02 Feb 2024 03:37:11 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 02 Feb 2024 03:37:11 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 02 Feb 2024 03:37:12 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 02 Feb 2024 03:37:12 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 02 Feb 2024 03:37:12 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 02 Feb 2024 03:37:12 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 02 Feb 2024 03:39:49 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 02 Feb 2024 03:39:52 GMT
EXPOSE 8000 9990
# Fri, 02 Feb 2024 03:39:52 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 02 Feb 2024 03:39:52 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21478c4a5959c6d09b8bb2d4ecf23304997c77e7f0b25d7d788dd3687b0aa0ae`  
		Last Modified: Fri, 02 Feb 2024 05:59:12 GMT  
		Size: 762.3 MB (762344120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3d379b00704865e167ee6ed4bd48e26ebe5b5d3646b1ec3ec0c824c1b66bb9`  
		Last Modified: Fri, 02 Feb 2024 05:57:50 GMT  
		Size: 4.0 MB (3994069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda3c1e4ba697069e9c4a2fa6ec14b1e31050c98205b52486f3b45d5eb277aa1`  
		Last Modified: Fri, 02 Feb 2024 05:57:50 GMT  
		Size: 7.1 MB (7146638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e3c0611b65a16b8b03c2b764137fdde10fc1bd2389efc88385acd68c9f5323`  
		Last Modified: Fri, 02 Feb 2024 05:57:48 GMT  
		Size: 2.5 MB (2534361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9a76f61979e562b65e217118d08791c247a62b4c0ee2730275e4f3300769ff`  
		Last Modified: Fri, 02 Feb 2024 05:57:47 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad309448567fc38f955ed2bbc664ee00e191e947bdb1ad81ebc455acd782b513`  
		Last Modified: Fri, 02 Feb 2024 05:57:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e27c20ed802868e85eec7b5d69c6653f82a932d881d02976c7c9707604d664`  
		Last Modified: Fri, 02 Feb 2024 05:57:59 GMT  
		Size: 217.8 MB (217842756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4242c478041451b10f1d7ade1069a03ba52ac7567afd178103573fe984a0ac`  
		Last Modified: Fri, 02 Feb 2024 05:57:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a844514597814ac8d447a395526f060bd5c985d4864fc52bcc30d79ee79bd3`  
		Last Modified: Fri, 02 Feb 2024 05:57:45 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c882e7c1d4c71a93689deb1ca2db910f6538352e3381e87258170c81866d5975`  
		Last Modified: Fri, 02 Feb 2024 05:57:45 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559eb6f0009904c42311adc9b39f9d2e8db3eb9872fe7a15e39999eee0425978`  
		Last Modified: Fri, 02 Feb 2024 05:57:45 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b71a40df7e7415893d48e1117dddfdda15bd94830d30590b3078be4b8785f93`  
		Last Modified: Fri, 02 Feb 2024 05:58:23 GMT  
		Size: 809.2 MB (809160681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:206a8c9041001ce65f0b8bd236e60e35e556aeab1a3d6578b814cda2b248614e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:463020dc703b6cba3c419d12a2de01ae655745865770c5af20a748b143d36c41
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1831609792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e07732c7a634ca2e1bbaceedd7a96532fda6b6f130d82f2be651e1c31d6da4`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Tue, 23 Jan 2024 13:01:02 GMT
ARG RELEASE
# Tue, 23 Jan 2024 13:01:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 23 Jan 2024 13:01:02 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 23 Jan 2024 13:01:04 GMT
ADD file:4b4e122c96445546ef9fba44a4eae6ada6239edecb9eea2c807a83abaebad451 in / 
# Tue, 23 Jan 2024 13:01:04 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 03:27:47 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 02 Feb 2024 03:27:47 GMT
ENV TERM=xterm
# Fri, 02 Feb 2024 03:35:45 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Fri, 02 Feb 2024 03:35:52 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Fri, 02 Feb 2024 03:35:56 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Fri, 02 Feb 2024 03:35:56 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 02 Feb 2024 03:36:34 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Fri, 02 Feb 2024 03:36:34 GMT
ENV LANG=en_US.UTF-8
# Fri, 02 Feb 2024 03:36:34 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 02 Feb 2024 03:36:34 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 02 Feb 2024 03:36:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Fri, 02 Feb 2024 03:36:35 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Fri, 02 Feb 2024 03:36:35 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 02 Feb 2024 03:36:36 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 02 Feb 2024 03:36:36 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 02 Feb 2024 03:36:36 GMT
ENV SILVERPEAS_VERSION=6.3.3
# Fri, 02 Feb 2024 03:36:36 GMT
ENV WILDFLY_VERSION=26.1.1
# Fri, 02 Feb 2024 03:36:36 GMT
LABEL name=Silverpeas 6.3.3 description=Image to install and to run Silverpeas 6.3.3 vendor=Silverpeas version=6.3.3 build=1
# Fri, 02 Feb 2024 03:37:11 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Fri, 02 Feb 2024 03:37:11 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Fri, 02 Feb 2024 03:37:12 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Fri, 02 Feb 2024 03:37:12 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 02 Feb 2024 03:37:12 GMT
COPY file:b54156953ecf6c3259f3b3d2885a784847c0996fd145c0f7ccef25182725511f in /opt/ 
# Fri, 02 Feb 2024 03:37:12 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Fri, 02 Feb 2024 03:39:49 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Fri, 02 Feb 2024 03:39:52 GMT
EXPOSE 8000 9990
# Fri, 02 Feb 2024 03:39:52 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 02 Feb 2024 03:39:52 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:3c67549075b6db92af85c8649f848d697b5bb1f448b436c4b4d6ee6834ab45f7`  
		Last Modified: Tue, 23 Jan 2024 18:44:22 GMT  
		Size: 28.6 MB (28584460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21478c4a5959c6d09b8bb2d4ecf23304997c77e7f0b25d7d788dd3687b0aa0ae`  
		Last Modified: Fri, 02 Feb 2024 05:59:12 GMT  
		Size: 762.3 MB (762344120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3d379b00704865e167ee6ed4bd48e26ebe5b5d3646b1ec3ec0c824c1b66bb9`  
		Last Modified: Fri, 02 Feb 2024 05:57:50 GMT  
		Size: 4.0 MB (3994069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda3c1e4ba697069e9c4a2fa6ec14b1e31050c98205b52486f3b45d5eb277aa1`  
		Last Modified: Fri, 02 Feb 2024 05:57:50 GMT  
		Size: 7.1 MB (7146638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7e3c0611b65a16b8b03c2b764137fdde10fc1bd2389efc88385acd68c9f5323`  
		Last Modified: Fri, 02 Feb 2024 05:57:48 GMT  
		Size: 2.5 MB (2534361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9a76f61979e562b65e217118d08791c247a62b4c0ee2730275e4f3300769ff`  
		Last Modified: Fri, 02 Feb 2024 05:57:47 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad309448567fc38f955ed2bbc664ee00e191e947bdb1ad81ebc455acd782b513`  
		Last Modified: Fri, 02 Feb 2024 05:57:47 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e27c20ed802868e85eec7b5d69c6653f82a932d881d02976c7c9707604d664`  
		Last Modified: Fri, 02 Feb 2024 05:57:59 GMT  
		Size: 217.8 MB (217842756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4242c478041451b10f1d7ade1069a03ba52ac7567afd178103573fe984a0ac`  
		Last Modified: Fri, 02 Feb 2024 05:57:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06a844514597814ac8d447a395526f060bd5c985d4864fc52bcc30d79ee79bd3`  
		Last Modified: Fri, 02 Feb 2024 05:57:45 GMT  
		Size: 663.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c882e7c1d4c71a93689deb1ca2db910f6538352e3381e87258170c81866d5975`  
		Last Modified: Fri, 02 Feb 2024 05:57:45 GMT  
		Size: 876.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559eb6f0009904c42311adc9b39f9d2e8db3eb9872fe7a15e39999eee0425978`  
		Last Modified: Fri, 02 Feb 2024 05:57:45 GMT  
		Size: 389.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b71a40df7e7415893d48e1117dddfdda15bd94830d30590b3078be4b8785f93`  
		Last Modified: Fri, 02 Feb 2024 05:58:23 GMT  
		Size: 809.2 MB (809160681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
