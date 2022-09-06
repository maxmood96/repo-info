## `maven:ibmjava`

```console
$ docker pull maven@sha256:c883d2f32ad7965baacc65bc7b8e2fbb25f1c5e02d6a8de80856419ffb73bca0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `maven:ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:a6b111a88e4912f3b93afe5caa69dfc2e9c36d10245b774132cfa114f72297af
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.9 MB (237894845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:093f064d13a68da631ad7c0d6383fba40d9244022c4be7d94ed139fbb94fe57a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 06 Sep 2022 19:38:36 GMT
ADD file:8733c7e8faf03d53cb2143ff6ac405362944cfa07422fccd21a3066cc2f42c83 in / 
# Tue, 06 Sep 2022 19:38:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 20:19:11 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 20:19:18 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:19:18 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 20:22:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 20:22:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 06 Sep 2022 22:14:19 GMT
RUN apt-get update && apt-get install -y curl
# Tue, 06 Sep 2022 22:14:19 GMT
ARG MAVEN_VERSION=3.8.6
# Tue, 06 Sep 2022 22:14:19 GMT
ARG USER_HOME_DIR=/root
# Tue, 06 Sep 2022 22:14:19 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Tue, 06 Sep 2022 22:14:19 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Tue, 06 Sep 2022 22:14:21 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 06 Sep 2022 22:14:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 06 Sep 2022 22:14:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 06 Sep 2022 22:14:21 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 06 Sep 2022 22:14:21 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 06 Sep 2022 22:14:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 06 Sep 2022 22:14:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:726b8a513d66e3585eb57389171d97fcd348e4914a415891e1da135b85ffa6c3`  
		Last Modified: Fri, 02 Sep 2022 15:41:13 GMT  
		Size: 26.7 MB (26710833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666a953ef9ff3115b0bc42a84f4510585612e4f86332b434b2a5e8382004df31`  
		Last Modified: Tue, 06 Sep 2022 20:22:22 GMT  
		Size: 3.0 MB (2957819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15018281f89c6806a00a38764f97f6ad50f6c0a9737ef2c20b086db436aa0567`  
		Last Modified: Tue, 06 Sep 2022 20:23:11 GMT  
		Size: 166.5 MB (166487132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2befb7bf4ff9001d93326f56c867851c0303c263675a939be7f833a9dd98b6b3`  
		Last Modified: Tue, 06 Sep 2022 22:16:50 GMT  
		Size: 33.0 MB (32998347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54d83353f8e6edad729b29680b4b1d757320f0fb047869df5dc738ddcf0137ec`  
		Last Modified: Tue, 06 Sep 2022 22:16:48 GMT  
		Size: 8.7 MB (8739506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe690dd5c15ff447844f15ef0752df5e0aa9cfc9c91d3e2769291dd45a6fd520`  
		Last Modified: Tue, 06 Sep 2022 22:16:47 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e5d9b057c6c63ae95c69ca5e495e29e40ba205a789a6ef7d789c6895f621a3`  
		Last Modified: Tue, 06 Sep 2022 22:16:47 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; 386

```console
$ docker pull maven@sha256:0534775100675d17644adff4a3b5512138d394ecfe5cf774813d8f7ceff14c20
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.5 MB (221520768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7760963f1ac4b8918e454446984f134ee08afa52dac534c1d8365baec878ec56`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 06 Sep 2022 18:40:06 GMT
ADD file:31701667cc90b9f4ce7d6ede94bf7dae4d63c49e62d3725094d547f9601e1165 in / 
# Tue, 06 Sep 2022 18:40:07 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 18:56:21 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 18:56:31 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 18:56:31 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 18:59:16 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 18:59:16 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 06 Sep 2022 19:16:15 GMT
RUN apt-get update && apt-get install -y curl
# Tue, 06 Sep 2022 19:16:16 GMT
ARG MAVEN_VERSION=3.8.6
# Tue, 06 Sep 2022 19:16:17 GMT
ARG USER_HOME_DIR=/root
# Tue, 06 Sep 2022 19:16:18 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Tue, 06 Sep 2022 19:16:19 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Tue, 06 Sep 2022 19:16:29 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 06 Sep 2022 19:16:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 06 Sep 2022 19:16:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 06 Sep 2022 19:16:33 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 06 Sep 2022 19:16:34 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 06 Sep 2022 19:16:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 06 Sep 2022 19:16:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:10d3032d1995d3163c20a7f2f197299fae258c2ad020a8fd586fd6b7dd1b0e1d`  
		Last Modified: Tue, 06 Sep 2022 18:40:53 GMT  
		Size: 27.2 MB (27164710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246b95ff97894a60bd98bbfe32df134abb0711c29aae72dd2607024590e794e8`  
		Last Modified: Tue, 06 Sep 2022 18:59:51 GMT  
		Size: 3.0 MB (2983211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:512724726918b6067a91dd1d2bb0a01890a704aa6e8ea39ce0a96938837acdc6`  
		Last Modified: Tue, 06 Sep 2022 19:00:48 GMT  
		Size: 154.5 MB (154498194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014d3e12c7cd8b422cc217c0fc8fed00736f4c9f2a45f10d87b0a21ff402cb93`  
		Last Modified: Tue, 06 Sep 2022 19:17:04 GMT  
		Size: 28.1 MB (28133975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a67e7c5b1ea2c62d592409cf40fd4d065d74c868602f6f3b4fcdc6f528d27c7a`  
		Last Modified: Tue, 06 Sep 2022 19:17:02 GMT  
		Size: 8.7 MB (8739467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632b9a8f9b751af76a883d1956144cab65ac95985fcced587515130f003c088c`  
		Last Modified: Tue, 06 Sep 2022 19:17:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef725a953eaef3adfef4bbbd0d7e9e9c59e9f762759b5223659f44ed5a13cf84`  
		Last Modified: Tue, 06 Sep 2022 19:17:01 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:0a53de91de73ef02a0b46d42b791ffc70c3f22e9eaf79ef676383c63e9aac0e2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **233.9 MB (233885308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5450a5de525fcfcea1a4ded030964aaf131cab459255456e61e79c204ddecfaa`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 06 Sep 2022 19:38:57 GMT
ADD file:1b76d0a41921afefb92711c44ceb312c16828d433b689a951d65c238faa9ac50 in / 
# Tue, 06 Sep 2022 19:38:59 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 20:20:27 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 20:20:38 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 20:20:38 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 20:28:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 20:28:32 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 06 Sep 2022 21:35:50 GMT
RUN apt-get update && apt-get install -y curl
# Tue, 06 Sep 2022 21:35:50 GMT
ARG MAVEN_VERSION=3.8.6
# Tue, 06 Sep 2022 21:35:51 GMT
ARG USER_HOME_DIR=/root
# Tue, 06 Sep 2022 21:35:51 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Tue, 06 Sep 2022 21:35:51 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Tue, 06 Sep 2022 21:35:53 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 06 Sep 2022 21:35:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 06 Sep 2022 21:35:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 06 Sep 2022 21:35:54 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 06 Sep 2022 21:35:55 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 06 Sep 2022 21:35:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 06 Sep 2022 21:35:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4abf8f40556a940861bc7fc313acefb89c775273ed06b7d41cfb222ccf8a1438`  
		Last Modified: Tue, 06 Sep 2022 19:40:56 GMT  
		Size: 30.4 MB (30441623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c293fce30924c9fe30d533e1b557627ce0453d0c3d2f3d7369e05d44a94eb7`  
		Last Modified: Tue, 06 Sep 2022 20:29:05 GMT  
		Size: 3.1 MB (3076075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca21b35ce07e2b858b11f89451c330fe2f52ca056867a0e08f250142b80264f6`  
		Last Modified: Tue, 06 Sep 2022 20:30:22 GMT  
		Size: 166.2 MB (166164093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30d12040f225ff095dbc26457389121a72e1114b64b6402f01d57fc296ec5ee`  
		Last Modified: Tue, 06 Sep 2022 21:38:06 GMT  
		Size: 25.5 MB (25462814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc1a010ae71ce0ef811ecfbb35b7792f8c46fbd50c04c97c5118185ebb430db`  
		Last Modified: Tue, 06 Sep 2022 21:38:03 GMT  
		Size: 8.7 MB (8739496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c18ef57155d40364c744b5ef9809539b881613d7bbf4b16773de7740b2159503`  
		Last Modified: Tue, 06 Sep 2022 21:38:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a442ad3fabb0484d7573e573a2b449bf07c983140a44db02c6fdf39d3e65f87`  
		Last Modified: Tue, 06 Sep 2022 21:38:02 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:689be506fe9811411a9889fbf1d1a847fbebffa27ce1ca4bef008be9afa1df09
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.0 MB (216977106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78598552a7e77b598916217d964407118f14dfca239beb5adb9356c8267eceed`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 06 Sep 2022 18:43:36 GMT
ADD file:dbe2a8e3943129e654ee29c636cab2bb10dd7eb0ac27d51e6954af2ccbe22807 in / 
# Tue, 06 Sep 2022 18:43:37 GMT
CMD ["bash"]
# Tue, 06 Sep 2022 19:00:40 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 06 Sep 2022 19:00:54 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Tue, 06 Sep 2022 19:00:55 GMT
ENV JAVA_VERSION=8.0.7.15
# Tue, 06 Sep 2022 19:03:33 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='f042fd06b9312001c7e19cf28194273f25cb5d2b2df4d864b1adfeffa3c8ae7d';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='cb3348717194f19dc08b38021aff2cdbda3e6911e8bcd8e953e909fa212922e4';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bee2e9e20657f22931e94981822af760c1a7d733134d2cb5dbc6b95bafac8f84';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='6731949f0d61182bc722ee23ba4b2784956afe65ff2ef26ea2e2e125bbff1ef7';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='496b90cdd5ebc279c8e3dbc1acc7c2c0fd8b4ca579ca4b10bbe9a6047b5009cb';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Tue, 06 Sep 2022 19:03:37 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 06 Sep 2022 19:24:24 GMT
RUN apt-get update && apt-get install -y curl
# Tue, 06 Sep 2022 19:24:24 GMT
ARG MAVEN_VERSION=3.8.6
# Tue, 06 Sep 2022 19:24:25 GMT
ARG USER_HOME_DIR=/root
# Tue, 06 Sep 2022 19:24:25 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Tue, 06 Sep 2022 19:24:25 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Tue, 06 Sep 2022 19:24:36 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 06 Sep 2022 19:24:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 06 Sep 2022 19:24:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 06 Sep 2022 19:24:37 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 06 Sep 2022 19:24:37 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 06 Sep 2022 19:24:37 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 06 Sep 2022 19:24:37 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:be6761156800c616810cb8aeb5b3ae71b9a2082f1c1221210befe119f082e879`  
		Last Modified: Tue, 06 Sep 2022 18:45:00 GMT  
		Size: 25.4 MB (25370130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85df87bfee2629b9bcbd6e19094a6bef3a7109cc473de2f41ee8e4f7d454d2b3`  
		Last Modified: Tue, 06 Sep 2022 19:04:07 GMT  
		Size: 2.7 MB (2671671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45f7c8c37bccd761caca18ceb0d6cce477753e96bf38f326628e381a5566b9aa`  
		Last Modified: Tue, 06 Sep 2022 19:04:50 GMT  
		Size: 156.8 MB (156760157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81f11783dc144b0f13dee61142b7424fe15ce412d4f1b7a33c2803e4148334b`  
		Last Modified: Tue, 06 Sep 2022 19:26:28 GMT  
		Size: 23.4 MB (23434441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:326ea487d143f14968fa18755c2cb1a49e0c9e2693d1ee3555b78f63dcb5e760`  
		Last Modified: Tue, 06 Sep 2022 19:26:27 GMT  
		Size: 8.7 MB (8739495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8a2543ec25ce8eb214a7b31e5d51cc2769dba6bd4bba3df712e948ef665890`  
		Last Modified: Tue, 06 Sep 2022 19:26:26 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b97b714982dff8516900fd7ed5670535c1a469772bed593ef772c1c48b4b30`  
		Last Modified: Tue, 06 Sep 2022 19:26:26 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
