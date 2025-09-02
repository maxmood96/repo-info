<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `silverpeas`

-	[`silverpeas:6.3.6`](#silverpeas636)
-	[`silverpeas:6.4.4`](#silverpeas644)
-	[`silverpeas:latest`](#silverpeaslatest)

## `silverpeas:6.3.6`

```console
$ docker pull silverpeas@sha256:ad4e77ecdc10c31064f4b3391fa5d246f273d605aabc6adf9e41ed88e31c24b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.3.6` - linux; amd64

```console
$ docker pull silverpeas@sha256:f7c76cfa0cfb0bfc54f9074103795b739b03fafbc1c981c265d64851127b8f79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1887122954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eef104de3cd2015a43c303d6a5665c338e3290fc3e753fabd4aa4c9bd1cf707`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 07 Aug 2025 15:06:13 GMT
ARG RELEASE
# Thu, 07 Aug 2025 15:06:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 07 Aug 2025 15:06:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 07 Aug 2025 15:06:13 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 07 Aug 2025 15:06:13 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Thu, 07 Aug 2025 15:06:13 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 15:06:13 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 07 Aug 2025 15:06:13 GMT
ENV TERM=xterm
# Thu, 07 Aug 2025 15:06:13 GMT
RUN apt-get update   && apt-get install -y tzdata   && apt-get install -y     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 *swftools-bin-0.9.2.zip' | sha256sum -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 *pdf2json-bin-0.68.zip' | sha256sum -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 07 Aug 2025 15:06:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 15:06:13 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 07 Aug 2025 15:06:13 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Aug 2025 15:06:13 GMT
ENV PING_ON=1
# Thu, 07 Aug 2025 15:06:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 07 Aug 2025 15:06:13 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 07 Aug 2025 15:06:13 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 07 Aug 2025 15:06:13 GMT
ENV SILVERPEAS_VERSION=6.3.6
# Thu, 07 Aug 2025 15:06:13 GMT
ENV WILDFLY_VERSION=26.1.1
# Thu, 07 Aug 2025 15:06:13 GMT
LABEL name=Silverpeas 6.3.6 description=Image to install and to run Silverpeas 6.3.6 vendor=Silverpeas version=6.3.6 build=2
# Thu, 07 Aug 2025 15:06:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 07 Aug 2025 15:06:13 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle   && ./silverpeas construct   && rm ../log/build-*   && touch .install # buildkit
# Thu, 07 Aug 2025 15:06:13 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 07 Aug 2025 15:06:13 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 07 Aug 2025 15:06:13 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7002116e30963fc5e07692480043b5676a6cd535bd8c31d0181f2e22862c36f0`  
		Last Modified: Tue, 02 Sep 2025 18:13:14 GMT  
		Size: 871.4 MB (871440690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c08d214082583246e5f08e12150d83530d37937a56aa13bcf5895437b2466dc`  
		Last Modified: Mon, 01 Sep 2025 23:18:40 GMT  
		Size: 4.0 MB (3994013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d7ef9e79737a4c52e20991d2ab786b192a411913bc3ec8e619cd2c67f2c65c`  
		Last Modified: Mon, 01 Sep 2025 23:18:37 GMT  
		Size: 7.1 MB (7146627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5734b323ed69d1dffa4bed48246c3a3e686a175ff5eec35585351bf031830e4e`  
		Last Modified: Mon, 01 Sep 2025 23:18:37 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183308fbdb2b8e6552337d4d6bfe338a4d6708d70f6aa225c998a96ec37f1ec2`  
		Last Modified: Mon, 01 Sep 2025 23:18:36 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76d4f3264671e79561c0018a92c4ef0ef71bb00f530f88053acc7012ce1e7130`  
		Last Modified: Mon, 01 Sep 2025 23:18:36 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ae13aa381750ede6c9f39617db96e67ea83e007632245fb81cb4dba1060801`  
		Last Modified: Tue, 02 Sep 2025 00:28:53 GMT  
		Size: 217.8 MB (217843285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16ec813f465c90628e0e978bf20df109b86ebe151526c6d3b31d55bca41d9430`  
		Last Modified: Mon, 01 Sep 2025 23:18:36 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72be3767200b6b94b283d75a0d2261f25dfd6c366bf3c7a3d6bce6a8e506a7c4`  
		Last Modified: Mon, 01 Sep 2025 23:18:36 GMT  
		Size: 662.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a1bc6bbf7b71d34ba8b468a3c7377e37a04950b6050806fba1392928ec66803`  
		Last Modified: Mon, 01 Sep 2025 23:18:36 GMT  
		Size: 921.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffdc3a3b16eb721e17c0a957f20091bbc5c85211078e13c8557a8a762536943`  
		Last Modified: Mon, 01 Sep 2025 23:18:36 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1197895311da2ddaa898b668b9d5340787a3393931db10acc70915eece2c030a`  
		Last Modified: Tue, 02 Sep 2025 00:29:35 GMT  
		Size: 754.6 MB (754620024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.3.6` - unknown; unknown

```console
$ docker pull silverpeas@sha256:c21423d87b5e8f4d08fe09ab4a8763dfb724b8b880e5bc1530843fa0a90fea29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26866145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:306197a1609e84867808dbd0d90943bdda5c9defe4d2b67b61b84c6418b0e00b`

```dockerfile
```

-	Layers:
	-	`sha256:1eac0954a55465c0e629a1c96b433d4c0562dce4b148344b1b6c66f4c43c9c32`  
		Last Modified: Tue, 02 Sep 2025 01:09:21 GMT  
		Size: 26.8 MB (26825400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4547b5633dd10f1ad9e84161ec71c7e86fa8452b06b02534976002efcd232c5d`  
		Last Modified: Tue, 02 Sep 2025 01:09:22 GMT  
		Size: 40.7 KB (40745 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:6.4.4`

```console
$ docker pull silverpeas@sha256:e3a7ffa1310cdd8d60a2a8cf7f152aeda5a1baf6932a4eb777726343da275283
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:6.4.4` - linux; amd64

```console
$ docker pull silverpeas@sha256:2501ee20fd2a414309b3aa2f136628292b387a92eba53c9ead43668350ed5392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817982288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38179dfa75c37ce9cf2acfca965d2d565f775ec9029414cbe693de9ad7e8def`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 07 Aug 2025 14:33:54 GMT
ARG RELEASE
# Thu, 07 Aug 2025 14:33:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 07 Aug 2025 14:33:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 07 Aug 2025 14:33:54 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 07 Aug 2025 14:33:54 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Thu, 07 Aug 2025 14:33:54 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 14:33:54 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 07 Aug 2025 14:33:54 GMT
ENV TERM=xterm
# Thu, 07 Aug 2025 14:33:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
ENV PING_ON=1
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 07 Aug 2025 14:33:54 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 07 Aug 2025 14:33:54 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 07 Aug 2025 14:33:54 GMT
ENV SILVERPEAS_VERSION=6.4.4
# Thu, 07 Aug 2025 14:33:54 GMT
ENV WILDFLY_VERSION=26.1.3
# Thu, 07 Aug 2025 14:33:54 GMT
LABEL name=Silverpeas 6.4.4 description=Image to install and to run Silverpeas 6.4.4 vendor=Silverpeas version=6.4.4 build=1
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 07 Aug 2025 14:33:54 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 07 Aug 2025 14:33:54 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc02b22a1e563ff9836a53bf87d28945f793f3125d2b490efa3b2e2388291db6`  
		Last Modified: Tue, 02 Sep 2025 16:07:54 GMT  
		Size: 494.8 MB (494793796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1432e514e2c63fb9db579a44b0405cdc03fe6676abadf1e145cff3d86cdfd`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 4.0 MB (3994014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371893ff3264e9da3f98819d40d49521d75e7e70ec5edb51fdb8305bf83ed8e`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 7.1 MB (7146619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c208ecc57d9d1c26987875e20863418755672210b33b54384da4081d0d900b`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 2.5 MB (2538610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95dd8459152c4dc6ef71b195a15c5424b23146674a5590354ac7e014cc0b330`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80f579011e4e990ed1196261335c9b634e62268f40c672a57325e72658e6b0`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fadf94384dfb380f1bda57c367c92ae527e7b9e83d9b5a2ad30f2b982d7a90`  
		Last Modified: Tue, 02 Sep 2025 16:10:39 GMT  
		Size: 269.1 MB (269106248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbebff4a17e428eff4acd2a20384a5e164f1d46e098bfec33f9d3aab04105cbd`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaea73ef07f4d24beab3f9c40074898215396acd62ba6e15a54055f4e458647`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 663.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d4cd9159887219d9a2e6818654c2f95c1f3f8d63fc8d97b3ce70ecd7780c01`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2e7ea58e7327c0df79cd2324594df28b4ff9f83765bd045371f5703287353`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a495523603157e520187211dd61d5dd97207e30e01ee2d06d2feaf52cf1f78a6`  
		Last Modified: Tue, 02 Sep 2025 16:12:16 GMT  
		Size: 1.0 GB (1010862770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:6.4.4` - unknown; unknown

```console
$ docker pull silverpeas@sha256:94215a6cb3d0fea22f0ce88cda161905cad881a112be11da55e87c30952fd146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e973bd97a2469238bb2d65ea275f51d9f6e5a0daedad4fa94dda172d653fc666`

```dockerfile
```

-	Layers:
	-	`sha256:bfd0e640b6a7a49b53c7d12e9e76725a89522b96d51f6af01bcc125474d0ba0d`  
		Last Modified: Tue, 02 Sep 2025 01:09:24 GMT  
		Size: 16.6 MB (16606161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c29c9b84aa2aefe2094c1a1924e7fa7641cd220fc4acf0a83c96348b55a4deb`  
		Last Modified: Tue, 02 Sep 2025 01:09:25 GMT  
		Size: 42.5 KB (42549 bytes)  
		MIME: application/vnd.in-toto+json

## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:e3a7ffa1310cdd8d60a2a8cf7f152aeda5a1baf6932a4eb777726343da275283
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:2501ee20fd2a414309b3aa2f136628292b387a92eba53c9ead43668350ed5392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817982288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e38179dfa75c37ce9cf2acfca965d2d565f775ec9029414cbe693de9ad7e8def`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Thu, 07 Aug 2025 14:33:54 GMT
ARG RELEASE
# Thu, 07 Aug 2025 14:33:54 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 07 Aug 2025 14:33:54 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 07 Aug 2025 14:33:54 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 07 Aug 2025 14:33:54 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Thu, 07 Aug 2025 14:33:54 GMT
CMD ["/bin/bash"]
# Thu, 07 Aug 2025 14:33:54 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 07 Aug 2025 14:33:54 GMT
ENV TERM=xterm
# Thu, 07 Aug 2025 14:33:54 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
ENV LANG=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 07 Aug 2025 14:33:54 GMT
ENV PING_ON=1
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 07 Aug 2025 14:33:54 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 07 Aug 2025 14:33:54 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 07 Aug 2025 14:33:54 GMT
ENV SILVERPEAS_VERSION=6.4.4
# Thu, 07 Aug 2025 14:33:54 GMT
ENV WILDFLY_VERSION=26.1.3
# Thu, 07 Aug 2025 14:33:54 GMT
LABEL name=Silverpeas 6.4.4 description=Image to install and to run Silverpeas 6.4.4 vendor=Silverpeas version=6.4.4 build=1
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Thu, 07 Aug 2025 14:33:54 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 07 Aug 2025 14:33:54 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 07 Aug 2025 14:33:54 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc02b22a1e563ff9836a53bf87d28945f793f3125d2b490efa3b2e2388291db6`  
		Last Modified: Tue, 02 Sep 2025 16:07:54 GMT  
		Size: 494.8 MB (494793796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5e1432e514e2c63fb9db579a44b0405cdc03fe6676abadf1e145cff3d86cdfd`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 4.0 MB (3994014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a371893ff3264e9da3f98819d40d49521d75e7e70ec5edb51fdb8305bf83ed8e`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 7.1 MB (7146619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c208ecc57d9d1c26987875e20863418755672210b33b54384da4081d0d900b`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 2.5 MB (2538610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b95dd8459152c4dc6ef71b195a15c5424b23146674a5590354ac7e014cc0b330`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba80f579011e4e990ed1196261335c9b634e62268f40c672a57325e72658e6b0`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fadf94384dfb380f1bda57c367c92ae527e7b9e83d9b5a2ad30f2b982d7a90`  
		Last Modified: Tue, 02 Sep 2025 16:10:39 GMT  
		Size: 269.1 MB (269106248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbebff4a17e428eff4acd2a20384a5e164f1d46e098bfec33f9d3aab04105cbd`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eaea73ef07f4d24beab3f9c40074898215396acd62ba6e15a54055f4e458647`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 663.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d4cd9159887219d9a2e6818654c2f95c1f3f8d63fc8d97b3ce70ecd7780c01`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cb2e7ea58e7327c0df79cd2324594df28b4ff9f83765bd045371f5703287353`  
		Last Modified: Mon, 01 Sep 2025 23:17:46 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a495523603157e520187211dd61d5dd97207e30e01ee2d06d2feaf52cf1f78a6`  
		Last Modified: Tue, 02 Sep 2025 16:12:16 GMT  
		Size: 1.0 GB (1010862770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:94215a6cb3d0fea22f0ce88cda161905cad881a112be11da55e87c30952fd146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e973bd97a2469238bb2d65ea275f51d9f6e5a0daedad4fa94dda172d653fc666`

```dockerfile
```

-	Layers:
	-	`sha256:bfd0e640b6a7a49b53c7d12e9e76725a89522b96d51f6af01bcc125474d0ba0d`  
		Last Modified: Tue, 02 Sep 2025 01:09:24 GMT  
		Size: 16.6 MB (16606161 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c29c9b84aa2aefe2094c1a1924e7fa7641cd220fc4acf0a83c96348b55a4deb`  
		Last Modified: Tue, 02 Sep 2025 01:09:25 GMT  
		Size: 42.5 KB (42549 bytes)  
		MIME: application/vnd.in-toto+json
