## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:dd08f14546f095ee882d4117e64aa2e94d6305ccf26664882917f51636f0bd81
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:255e6ace65bcf1124c3c94203a012214c6d278bd1f5430854a735db4ceb85e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1818274739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20267922e5c1ae699030e17279cc135bd9d3045bcfed7cf593c5b692d30d36af`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Sun, 22 Mar 2026 18:10:35 GMT
ARG RELEASE
# Sun, 22 Mar 2026 18:10:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sun, 22 Mar 2026 18:10:35 GMT
LABEL org.opencontainers.image.version=22.04
# Sun, 22 Mar 2026 18:10:38 GMT
ADD file:6d6bdec36f3282e8506d4ebfcecc427191e59c9cf197a51a9e5787e7490eb0d6 in / 
# Sun, 22 Mar 2026 18:10:38 GMT
CMD ["/bin/bash"]
# Wed, 01 Apr 2026 20:19:03 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Wed, 01 Apr 2026 20:19:03 GMT
ENV TERM=xterm
# Wed, 01 Apr 2026 20:19:03 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Wed, 01 Apr 2026 20:19:05 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Wed, 01 Apr 2026 20:19:08 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Wed, 01 Apr 2026 20:19:08 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Wed, 01 Apr 2026 20:19:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Wed, 01 Apr 2026 20:19:30 GMT
ENV LANG=en_US.UTF-8
# Wed, 01 Apr 2026 20:19:30 GMT
ENV LANGUAGE=en_US.UTF-8
# Wed, 01 Apr 2026 20:19:30 GMT
ENV LC_ALL=en_US.UTF-8
# Wed, 01 Apr 2026 20:19:30 GMT
ENV PING_ON=1
# Wed, 01 Apr 2026 20:19:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Wed, 01 Apr 2026 20:19:30 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Wed, 01 Apr 2026 20:19:30 GMT
ENV JAVA_HOME=/docker-java-home
# Wed, 01 Apr 2026 20:19:30 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Wed, 01 Apr 2026 20:19:30 GMT
ENV JBOSS_HOME=/opt/wildfly
# Wed, 01 Apr 2026 20:19:30 GMT
ENV SILVERPEAS_VERSION=6.4.6
# Wed, 01 Apr 2026 20:19:30 GMT
ENV WILDFLY_VERSION=26.1.3
# Wed, 01 Apr 2026 20:19:30 GMT
LABEL name=Silverpeas 6.4.6 description=Image to install and to run Silverpeas 6.4.6 vendor=Silverpeas version=6.4.6 build=1
# Wed, 01 Apr 2026 20:19:53 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Wed, 01 Apr 2026 20:19:53 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Wed, 01 Apr 2026 20:19:53 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Wed, 01 Apr 2026 20:19:53 GMT
WORKDIR /opt/silverpeas/bin
# Wed, 01 Apr 2026 20:19:53 GMT
COPY src/run.sh /opt/ # buildkit
# Wed, 01 Apr 2026 20:19:53 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Wed, 01 Apr 2026 20:21:20 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Wed, 01 Apr 2026 20:21:20 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Wed, 01 Apr 2026 20:21:20 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Wed, 01 Apr 2026 20:21:20 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:de47083ed7d7e66ba5116fed0a5b036b7c75ac74b2cfb0d9c3b89c79371c4a17`  
		Last Modified: Sun, 22 Mar 2026 18:43:25 GMT  
		Size: 29.7 MB (29736413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:805208d8fa47d98fc06f05e2b9180b89b8560a52ffcf077194a98c07a7d9aa26`  
		Last Modified: Wed, 01 Apr 2026 20:23:00 GMT  
		Size: 494.9 MB (494881466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:786b7202c84187ddc12ad0947ad5eee94409c37b1e4748a8e9cd79eb6e36d850`  
		Last Modified: Wed, 01 Apr 2026 20:22:43 GMT  
		Size: 4.0 MB (3994013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2157e34b2109ea7b0b91a2775a4ad9b38f363a729d4c7549c90b82e4800aaada`  
		Last Modified: Wed, 01 Apr 2026 20:22:43 GMT  
		Size: 7.1 MB (7146638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b12657277f0110878b83099b22906b5106089c18f30ca4020f33affe573443`  
		Last Modified: Wed, 01 Apr 2026 20:22:43 GMT  
		Size: 2.5 MB (2538614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9f3c25654821f24b508217669cd8ab6bc39ac62e0c624bf4c262b56c1e13d7`  
		Last Modified: Wed, 01 Apr 2026 20:22:44 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b623b7470bd233784cce623ec1566db3c30495a746e2f9a63509d72099081fb2`  
		Last Modified: Wed, 01 Apr 2026 20:22:44 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17b9065bd5f775b9661762a16f6b839742c5dbf307ca0d23f1030de294e7ecd6`  
		Last Modified: Wed, 01 Apr 2026 20:22:56 GMT  
		Size: 269.1 MB (269106279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1e0fcbe116e3f00f9b8f84dc18f4f8082564ff63f1ef4070d101849edb2db8e`  
		Last Modified: Wed, 01 Apr 2026 20:22:45 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c272cca84e67206eb4412a7df51e8fc2217583d72aa8b9b6afbc197b8a77bf2`  
		Last Modified: Wed, 01 Apr 2026 20:22:45 GMT  
		Size: 664.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2424177414bbbf7292c4bb7ee3be481b3c55b6e5e96c9ff9ed8f3105679597c3`  
		Last Modified: Wed, 01 Apr 2026 20:22:47 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e8fa4cacc0fd88eb0083e17176c69191ece74c7ad68abc2bdb448ed9a405e5`  
		Last Modified: Wed, 01 Apr 2026 20:22:47 GMT  
		Size: 385.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c11f9b7569abe911fc67af963aa64f912233d0208f6b9b826a661d95d7747f`  
		Last Modified: Wed, 01 Apr 2026 20:23:14 GMT  
		Size: 1.0 GB (1010868016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:9a13579d964793d822e61aaf7196132f6a638e55416a44060fda1999c20fd56c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16648828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53cb26af3bc060ae64093778dafe1192f20738b51ce4540f2b6414a4a729abaa`

```dockerfile
```

-	Layers:
	-	`sha256:01c267704044a58c60d16d1530f710bee718deb2dc90f5358cd0b430e7cabf3b`  
		Last Modified: Wed, 01 Apr 2026 20:22:43 GMT  
		Size: 16.6 MB (16606322 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2100c7836da19b8fd041919a9510bff29a1d1ae163999e89e654653b8ad48ecf`  
		Last Modified: Wed, 01 Apr 2026 20:22:42 GMT  
		Size: 42.5 KB (42506 bytes)  
		MIME: application/vnd.in-toto+json
