## `silverpeas:latest`

```console
$ docker pull silverpeas@sha256:e3204edd730f297d080da112be0018734e895468c697731408e152596b6a073d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `silverpeas:latest` - linux; amd64

```console
$ docker pull silverpeas@sha256:3f89d31f4a488da2b57cf45a69c00f2abbf483775482f0e840f76bb8b5ba9ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1798666237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c1b640b2049ff9302301dcd612859ebeb7ff792812de81f790db50c35c65f7`
-	Default Command: `["\/opt\/run.sh"]`

```dockerfile
# Wed, 11 Sep 2024 16:25:16 GMT
ARG RELEASE
# Wed, 11 Sep 2024 16:25:16 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 11 Sep 2024 16:25:16 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 11 Sep 2024 16:25:17 GMT
ADD file:ebe009f86035c175ba244badd298a2582914415cf62783d510eab3a311a5d4e1 in / 
# Wed, 11 Sep 2024 16:25:18 GMT
CMD ["/bin/bash"]
# Thu, 12 Dec 2024 09:44:16 GMT
MAINTAINER Miguel Moquillon "miguel.moquillon@silverpeas.org"
# Thu, 12 Dec 2024 09:44:16 GMT
ENV TERM=xterm
# Thu, 12 Dec 2024 09:44:16 GMT
RUN apt-get update   && apt-get install -y --no-install-recommends tzdata   && apt-get install -y --no-install-recommends     apt-utils     iputils-ping     curl     wget     vim     locales     language-pack-en     language-pack-fr     procps     net-tools     zip     unzip     openjdk-11-jdk     ffmpeg     imagemagick     ghostscript     libreoffice     ure     gpgv   && rm -rf /var/lib/apt/lists/*   && update-ca-certificates -f # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
RUN wget -nc https://www.silverpeas.org/files/swftools-bin-0.9.2.zip   && echo 'd40bd091c84bde2872f2733a3c767b3a686c8e8477a3af3a96ef347cf05c5e43 swftools-bin-0.9.2.zip' | sha256sum -c --status -   && unzip swftools-bin-0.9.2.zip -d /   && rm swftools-bin-0.9.2.zip # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
RUN wget -nc https://www.silverpeas.org/files/pdf2json-bin-0.68.zip   && echo 'eec849cdd75224f9d44c0999ed1fbe8764a773d8ab0cf7fff4bf922ab81c9f84 pdf2json-bin-0.68.zip' | sha256sum -c --status -   && unzip pdf2json-bin-0.68.zip -d /   && rm pdf2json-bin-0.68.zip # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
ARG DEFAULT_LOCALE=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen   && echo "fr_FR.UTF-8 UTF-8" >> /etc/locale.gen   && echo "de_DE.UTF-8 UTF-8" >> /etc/locale.gen   && locale-gen   && update-locale LANG=${DEFAULT_LOCALE} LANGUAGE=${DEFAULT_LOCALE} LC_ALL=${DEFAULT_LOCALE} # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
ENV LANG=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
ENV LANGUAGE=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
ENV LC_ALL=en_US.UTF-8
# Thu, 12 Dec 2024 09:44:16 GMT
ENV PING_ON=1
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN { 		echo '#!/bin/sh'; 		echo 'set -e'; 		echo; 		echo 'dirname "$(dirname "$(readlink -f "$(which javac || which java)")")"'; 	} > /usr/local/bin/docker-java-home 	&& chmod +x /usr/local/bin/docker-java-home # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN ln -svT "/usr/lib/jvm/java-11-openjdk-$(dpkg --print-architecture)" /docker-java-home # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
ENV JAVA_HOME=/docker-java-home
# Thu, 12 Dec 2024 09:44:16 GMT
ENV SILVERPEAS_HOME=/opt/silverpeas
# Thu, 12 Dec 2024 09:44:16 GMT
ENV JBOSS_HOME=/opt/wildfly
# Thu, 12 Dec 2024 09:44:16 GMT
ENV SILVERPEAS_VERSION=6.4.2
# Thu, 12 Dec 2024 09:44:16 GMT
ENV WILDFLY_VERSION=26.1.3
# Thu, 12 Dec 2024 09:44:16 GMT
LABEL name=Silverpeas 6.4.2 description=Image to install and to run Silverpeas 6.4.2 vendor=Silverpeas version=6.4.2 build=1
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc   && gpg --keyserver keys.openpgp.org --recv-keys 3F4657EF9C591F2FEA458FEBC19391EB3DF442B6   && gpg --batch --verify silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip.asc silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip   && wget -nc https://www.silverpeas.org/files/wildfly-${WILDFLY_VERSION}.Final.zip   && unzip silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?}.zip -d /opt   && unzip wildfly-${WILDFLY_VERSION}.Final.zip -d /opt   && mv /opt/silverpeas-${SILVERPEAS_VERSION}-wildfly${WILDFLY_VERSION%.?.?} /opt/silverpeas   && mv /opt/wildfly-${WILDFLY_VERSION}.Final /opt/wildfly   && wget -nc https://www.silverpeas.org/files/oak-migrate.zip   && echo '87009e55520e74b5d2a386f4ebc843ee43cd1f25ca5138f342a94a31add3cfbd oak-migrate.zip' | sha256sum -c --status -   && mkdir -p /opt/oak-migration   && unzip oak-migrate.zip -d /opt/oak-migration/   && chmod +x /opt/oak-migration/oak-migrate.sh   && rm *.zip   && mkdir -p /root/.m2 # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/settings.xml /root/.m2/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/silverpeas.gradle /opt/silverpeas/bin/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
WORKDIR /opt/silverpeas/bin
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/run.sh /opt/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
COPY src/converter.groovy /opt/silverpeas/configuration/silverpeas/ # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
# ARGS: DEFAULT_LOCALE=en_US.UTF-8
RUN set -eux;   sed -i -e "s/SILVERPEAS_VERSION/${SILVERPEAS_VERSION}/g" ${SILVERPEAS_HOME}/bin/silverpeas.gradle;   echo "Construct Silverpeas ${SILVERPEAS_VERSION}";   ./silverpeas assemble || (cat ../log/build-* && exit 1);   rm ../log/build-*;   touch .install; # buildkit
# Thu, 12 Dec 2024 09:44:16 GMT
EXPOSE map[8000/tcp:{} 9990/tcp:{}]
# Thu, 12 Dec 2024 09:44:16 GMT
VOLUME [/opt/silverpeas/log /opt/silverpeas/data /opt/silverpeas/properties /opt/silverpeas/xmlcomponents/workflows]
# Thu, 12 Dec 2024 09:44:16 GMT
CMD ["/opt/run.sh"]
```

-	Layers:
	-	`sha256:6414378b647780fee8fd903ddb9541d134a1947ce092d08bdeb23a54cb3684ac`  
		Last Modified: Wed, 11 Sep 2024 17:24:41 GMT  
		Size: 29.5 MB (29535688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e526b1f2bd03f225de92ee95ba1d872d9d8ae6e1339ee9dddda6a09af6d301`  
		Last Modified: Thu, 12 Dec 2024 19:32:37 GMT  
		Size: 495.0 MB (494970681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c04dfb2ce7107e94873d6e44b4ddfcd59c18c28fbffcc2a97c90b1abf12f0b04`  
		Size: 4.0 MB (3994012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26d2dc201d58da95ddd695dff3a0313bad84f1ddf6f0f9c2d6cffe1e7f379a7d`  
		Last Modified: Thu, 12 Dec 2024 19:32:30 GMT  
		Size: 7.1 MB (7146616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12765cc063a01ea65ad5193082096fb7ab7db2ebb9a138714a65394c261eebf2`  
		Size: 2.5 MB (2538613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a6ae83999e6cf7899ece1f9c04e0bc5968a3d9991f882f53199fa881fbecc2`  
		Last Modified: Wed, 08 Jan 2025 00:01:32 GMT  
		Size: 235.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a822fc87adf6a77502d4c07cc060d3ef30f851ce4101d385d7ca0e9428c9b547`  
		Last Modified: Thu, 12 Dec 2024 19:32:31 GMT  
		Size: 131.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ba68912f00400fc149a83d263d8d23750f3bb6b2033b2a638ffc5f0b6003e1`  
		Last Modified: Thu, 12 Dec 2024 19:32:34 GMT  
		Size: 269.1 MB (269106217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7a2d60b0c60765780921a2382843b1bed261c5e7cf5922cac01fcfc18b0ff3`  
		Last Modified: Thu, 12 Dec 2024 19:32:31 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1289b516a4edba60cb4358b9423ea9df6c2844fd2ecda5191136e41534fc992a`  
		Last Modified: Thu, 12 Dec 2024 19:32:31 GMT  
		Size: 657.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fc142d372a7c7b8875705f061f536542d5515f51322b2040d01341a56515089`  
		Last Modified: Thu, 12 Dec 2024 19:32:32 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2298ba873ed7ba06dc3865bfacab423daa5f7b334e300171346ae7d976cc3011`  
		Size: 383.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975ebd412527ca6208d11b3d712ce00531a807cbcd2496ed1831c88942c70695`  
		Last Modified: Thu, 12 Dec 2024 19:32:47 GMT  
		Size: 991.4 MB (991371121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `silverpeas:latest` - unknown; unknown

```console
$ docker pull silverpeas@sha256:ae5536bec6116c7beee5aa13ea8e780d4ba38eac9a83af1bbb92b2aafcb63e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15742751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a3ada9afc57be6e92cfedec7d9bf778abcb640a3d61d96d6ab9357a2e5289d`

```dockerfile
```

-	Layers:
	-	`sha256:becdc3099ed32636653d9102d87036608c9b9b6a13c07446b6866395264e2776`  
		Last Modified: Thu, 12 Dec 2024 19:32:30 GMT  
		Size: 15.7 MB (15700204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2855c5c5c36b78a5b0905870a266094bcc3435d6791629c436879448dfad94f4`  
		Last Modified: Thu, 12 Dec 2024 19:32:30 GMT  
		Size: 42.5 KB (42547 bytes)  
		MIME: application/vnd.in-toto+json
