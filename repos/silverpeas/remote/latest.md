## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:ab0aa3e5a5feb00dbd3ec5eaa79eaec0adf1606b02ba7e0ea9caaf21f8395049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:b956b1b6845b58bd53a8e6483defe02e3e1b91488958659ade9913a4acba53f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1777030461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47b721661c97cc497ffe5a96e701fa10d7cd7a0c28580a77945fab3c89cd8034`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 16 Feb 2024 21:32:49 GMT
ARG RELEASE
# Fri, 16 Feb 2024 21:32:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 16 Feb 2024 21:32:49 GMT
LABEL org.opencontainers.image.version=20.04
# Fri, 16 Feb 2024 21:32:52 GMT
ADD file:a25798f31219000d6a82d2c9258743926b1a400530d12dbb1eadf2c2519f9888 in / 
# Fri, 16 Feb 2024 21:32:52 GMT
CMD ["/bin/bash"]
# Wed, 06 Mar 2024 05:33:41 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 06 Mar 2024 05:33:41 GMT
ENV TERM=xterm
# Wed, 06 Mar 2024 05:41:14 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f
# Wed, 06 Mar 2024 05:41:19 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip
# Wed, 06 Mar 2024 05:41:22 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip
# Wed, 06 Mar 2024 05:41:23 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 06 Mar 2024 05:42:02 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE}
# Wed, 06 Mar 2024 05:42:03 GMT
ENV LANG=en_US.UTF-8
# Wed, 06 Mar 2024 05:42:03 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 06 Mar 2024 05:42:03 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 06 Mar 2024 05:42:03 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home
# Wed, 06 Mar 2024 05:42:04 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home
# Wed, 06 Mar 2024 05:42:04 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 06 Mar 2024 05:42:04 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 06 Mar 2024 05:42:04 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 06 Mar 2024 05:42:04 GMT
ENV SILVERPEAS_VERSION=6.3.4
# Wed, 06 Mar 2024 05:42:04 GMT
ENV WILDFLY_VERSION=26.1.1
# Wed, 06 Mar 2024 05:42:04 GMT
LABEL name=Silverpeas 6.3.4 description=Image to install and to run Silverpeas 6.3.4 vendor=Silverpeas version=6.3.4 build=1
# Wed, 06 Mar 2024 05:42:38 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2
# Wed, 06 Mar 2024 05:42:38 GMT
COPY file:4d0e637a3e1ce0b8143795fd5df1997a7ee18fba27382849ed23e9ecb8142009 in /root/.m2/ 
# Wed, 06 Mar 2024 05:42:38 GMT
COPY file:473bf75b335a39b6b4b39c64cd151bd8ed3d3e33da73b8124e537a5db1fad3d6 in /opt/silverpeas/bin/ 
# Wed, 06 Mar 2024 05:42:39 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 06 Mar 2024 05:42:39 GMT
COPY file:53a5e8023ae593585b413b14c995a55c412d5a4dff0ebcb7db632f2c22c39da6 in /opt/ 
# Wed, 06 Mar 2024 05:42:39 GMT
COPY file:b5a807d0a061fd9e87c6acfc7080c110a5f3c030251fe9a4c995cec7603e12d2 in /opt/silverpeas/configuration/silverpeas/ 
# Wed, 06 Mar 2024 05:45:10 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install
# Wed, 06 Mar 2024 05:45:13 GMT
EXPOSE 8000 9990
# Wed, 06 Mar 2024 05:45:13 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 06 Mar 2024 05:45:13 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:63e9bbe323274e77e58d77c6ab6802d247458f784222fbb07a2556d6ec74ee05`  
		Last Modified: Sat, 17 Feb 2024 02:07:52 GMT  
		Size: 28.6 MB (28584317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36b06d973373245e4d8ba2a7d568f0eddb1042668921fe683aa78e35e8c52c59`  
		Last Modified: Wed, 06 Mar 2024 05:46:51 GMT  
		Size: 762.4 MB (762367403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd4b46a224e387376d6ba1178be2751b3d981bf152087548bd05aad4092cf8e`  
		Last Modified: Wed, 06 Mar 2024 05:45:29 GMT  
		Size: 4.0 MB (3994070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b410a7f29f7f9c03b4d116af73c94100c434b47bb09bba31797a3ff04096e668`  
		Last Modified: Wed, 06 Mar 2024 05:45:30 GMT  
		Size: 7.1 MB (7146645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c95c9befad7c33b43b20480d71b9d5d618d99831112a24bafcc82cc68c320a2f`  
		Last Modified: Wed, 06 Mar 2024 05:45:27 GMT  
		Size: 2.5 MB (2534359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96551efad5fba45a0daab4d953ec8aa510d9ef331ff3b3aa9b2660514397c98`  
		Last Modified: Wed, 06 Mar 2024 05:45:27 GMT  
		Size: 243.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:206c11de2cabec3a580cb1805d43fcf5ec7a2678f9b3e1da1ee52645bd9501e4`  
		Last Modified: Wed, 06 Mar 2024 05:45:27 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9815a0ce8bebeee16e48c39682c3145b2362078f96e0b130dfa627cb958529`  
		Last Modified: Wed, 06 Mar 2024 05:45:38 GMT  
		Size: 217.8 MB (217842685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b57db74d4e07b8fc3bbc057fa7b64b8d10a9d9956f58faa74b9968fdfc3c0da9`  
		Last Modified: Wed, 06 Mar 2024 05:45:25 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01512619965624b77da9b98b62384303f24988a773b8e52893bb51b237d67ff3`  
		Last Modified: Wed, 06 Mar 2024 05:45:25 GMT  
		Size: 661.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b9a664129ff8745baf567f69d9d6526bee1a54cda7fdc26b60fc8c71e7b8d6`  
		Last Modified: Wed, 06 Mar 2024 05:45:25 GMT  
		Size: 908.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a113ba1f8409d3f9a84202eff74f01b8ef522ff9c61af529e2dc539755943ae9`  
		Last Modified: Wed, 06 Mar 2024 05:45:25 GMT  
		Size: 384.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa8ab7560e5db5441de727bd0223de7a47a989064d8b912a7aedbceabad2bd81`  
		Last Modified: Wed, 06 Mar 2024 05:46:04 GMT  
		Size: 754.6 MB (754558253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
