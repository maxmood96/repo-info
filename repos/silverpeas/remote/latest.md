## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:cf013504b14d80e8937687212f0f8af62c22d3a7c5567e348288b427dbdbf866
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:67c280f70bb0cb1c1af7805dc79fb0dfbe66dbd405a25dfd861190df69c62689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1817814971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ebdcc762c3020bef88f073773c343274691002cd2b763de5534a346ce23adc`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Fri, 11 Apr 2025 14:37:01 GMT
ARG RELEASE
# Fri, 11 Apr 2025 14:37:01 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 11 Apr 2025 14:37:01 GMT
ADD file:59e67123ba6a5d9eea9813e7b2a767696f767c15c5b23c61c4d5bd6ba6fa9ac6 in / 
# Fri, 11 Apr 2025 14:37:01 GMT
CMD ["/bin/bash"]
# Fri, 11 Apr 2025 14:37:01 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Fri, 11 Apr 2025 14:37:01 GMT
ENV TERM=xterm
# Fri, 11 Apr 2025 14:37:01 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANG=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LANGUAGE=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV LC_ALL=en_US.UTF-8
# Fri, 11 Apr 2025 14:37:01 GMT
ENV PING_ON=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JAVA_HOME=/docker-java-home
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Fri, 11 Apr 2025 14:37:01 GMT
ENV JBOSS_HOME=/opt/wildfly
# Fri, 11 Apr 2025 14:37:01 GMT
ENV SILVERPEAS_VERSION=6.4.3
# Fri, 11 Apr 2025 14:37:01 GMT
ENV WILDFLY_VERSION=26.1.3
# Fri, 11 Apr 2025 14:37:01 GMT
LABEL name=Silverpeas 6.4.3 description=Image to install and to run Silverpeas 6.4.3 vendor=Silverpeas version=6.4.3 build=1
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
WORKDIR /opt/silverpeas/bin
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/run.sh /opt/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Fri, 11 Apr 2025 14:37:01 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Fri, 11 Apr 2025 14:37:01 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Fri, 11 Apr 2025 14:37:01 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:215ed5a638430309375291c48a01872859a8dbf1331e54ba0af221918eb8ce2e`  
		Last Modified: Mon, 28 Apr 2025 10:43:45 GMT  
		Size: 29.5 MB (29532614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ceed19b43f2a59dc614495dc95ecebfe83cf02e94ed579f7d76bad187279d8`  
		Last Modified: Mon, 05 May 2025 16:42:13 GMT  
		Size: 494.7 MB (494716196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e944e16eb062d3fb99991535738452559e6864c398a6b8a76e355f22f21b3e8`  
		Last Modified: Mon, 05 May 2025 16:42:05 GMT  
		Size: 4.0 MB (3994012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c9449561604d6234ba9eb2fbf6b13adb93a0469c5cb3c59aa08b9b72684b187`  
		Last Modified: Mon, 05 May 2025 16:42:05 GMT  
		Size: 7.1 MB (7146623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e99245ed9137b7dc96cc3feb9e2a253d8cf829dd6c3f5a575f1cedcc7e62d52`  
		Last Modified: Mon, 05 May 2025 16:42:05 GMT  
		Size: 2.5 MB (2538615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a4e07cb4f0f36063a78eb8c516458b47cd9e8bceeba1165f925c75beed40b1`  
		Last Modified: Mon, 05 May 2025 16:42:06 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a68c5116f310870afae2d0d4f6d4fa4ec593146ed5c8fb4e779809c615b7d7`  
		Last Modified: Mon, 05 May 2025 16:42:06 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4799da231892e54fbd39a0be3d18c2cccd03caa67267b93ed7d8ac378ce7848`  
		Last Modified: Mon, 05 May 2025 16:42:10 GMT  
		Size: 269.1 MB (269106225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:262b9545dc533dd8c5aaee9942cdf7af15eaff2d511dbd8787cab823974d288a`  
		Last Modified: Mon, 05 May 2025 16:42:07 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0fe9565901fd8da2a31c4c8c35227cfcab6043e7451063dc029cca22a84c8f`  
		Last Modified: Mon, 05 May 2025 16:42:06 GMT  
		Size: 662.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1dca20faa631eacafce31deaa1ee0f334c8e52225c4a594a53c10239a420a1`  
		Last Modified: Mon, 05 May 2025 16:42:07 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76bfd95526f777b6606fe32f4b25089d56cdbfbdeb76515a56d3ce543554b734`  
		Last Modified: Mon, 05 May 2025 16:42:07 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e53fa593cd08b4e030498a92121eb45800181e47d8c1b278ca37d417c93bed`  
		Last Modified: Mon, 05 May 2025 16:42:24 GMT  
		Size: 1.0 GB (1010777391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:0e7c2f3b436b928fac6778c8fb510284008c475d30933bdc1e7352bf26dbf6ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15747084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54bd21376158b5a049d719da95af7fcfa88ec7342bde917b804c03f8f00d35d5`

```dockerfile
```

-	Layers:
	-	`sha256:bc9eecc6dea65d3986cc38f12c56440a8d6da472915c473ff0bf5df055077d9f`  
		Last Modified: Mon, 05 May 2025 16:42:05 GMT  
		Size: 15.7 MB (15704535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:719f8b73041f59eaf78a80216ea440302566b99092f7ea596dea9271a4051cfa`  
		Last Modified: Mon, 05 May 2025 16:42:05 GMT  
		Size: 42.5 KB (42549 bytes)  
		MIME: application/vnd.in-toto+json
