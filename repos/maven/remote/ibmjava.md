## `maven:ibmjava`

```console
$ docker pull maven@sha256:c5f681e7a42f7b2a4109cf0fb44b638d851b917b11089d96d7a5f1220ab0d800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `maven:ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:2b852b8f90d5c509afe3e8fe803127d07bee19fb57201bc8ed283377b144422f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.1 MB (238095973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec6a8594b116b72772ec6b4e063592d006f645718262ae58481d23db75232f75`
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
# Wed, 28 Sep 2022 00:41:44 GMT
ENV JAVA_VERSION=8.0.7.16
# Wed, 28 Sep 2022 00:44:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb34f647a77ae43611dab3a447da447686352da5426baaff26c22a465dfe40c0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='b8c35301b56fde151b14e1bfb1374f579f5a0ed361d6ebc7ffff5f82eb563344';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='79fde4473b2c489278fdef105bf69097f1f1a0d54d75a59d24008773b512339b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f1989ee7f41d8d697e880dea74f94133841c2f59ded5c9dd551a26b87f4d36cf';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='eb1cd5b6bf532f10558e7067768d14884d9fce375d2782f91b2218365152bc42';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 28 Sep 2022 00:44:43 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 28 Sep 2022 01:30:41 GMT
RUN apt-get update && apt-get install -y curl
# Wed, 28 Sep 2022 01:30:42 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 28 Sep 2022 01:30:42 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Sep 2022 01:30:42 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 28 Sep 2022 01:30:42 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 28 Sep 2022 01:30:45 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 28 Sep 2022 01:30:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Sep 2022 01:30:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Sep 2022 01:30:45 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 28 Sep 2022 01:30:46 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 28 Sep 2022 01:30:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Sep 2022 01:30:46 GMT
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
	-	`sha256:5e4a8cd9063f80a8d4c89f15af36a2a2e3f5be2577ef20766810aec5447a1bcf`  
		Last Modified: Wed, 28 Sep 2022 00:45:57 GMT  
		Size: 166.5 MB (166497648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15747344ef482e31aca5edd5c3acd3471cd0c064cbba4e6a60648decccab74c6`  
		Last Modified: Wed, 28 Sep 2022 01:33:06 GMT  
		Size: 33.2 MB (33188959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc67b41a53412439ff5a0e45f348cfeab80ac0b2fe13df0f07d9873f9207e4c5`  
		Last Modified: Wed, 28 Sep 2022 01:33:04 GMT  
		Size: 8.7 MB (8739499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada940b411031f5a81949b3a09e6a7c7ae44c65367df3b4869c2b2862c499bb9`  
		Last Modified: Wed, 28 Sep 2022 01:33:03 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2db0db4b16adb70c5820ed3af8fa852ee304bc8c56e202b4cb66e0016737d2f`  
		Last Modified: Wed, 28 Sep 2022 01:33:03 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; 386

```console
$ docker pull maven@sha256:9d71ddeefd98c6f444fac143d0eadaaea3529856c9555739c0f0f57fee4489bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.6 MB (221631911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a5906c3ee986f8188797efc3abf0e3604b906a3a80719311c3baf8ee02ac33`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 04 Oct 2022 23:51:15 GMT
ADD file:ee35e95b906b98c2d7493d8c365bf5aaf351251abce763f9be2d9fa6cc541aaf in / 
# Tue, 04 Oct 2022 23:51:15 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 14:18:49 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 05 Oct 2022 14:19:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 14:19:08 GMT
ENV JAVA_VERSION=8.0.7.16
# Wed, 05 Oct 2022 14:21:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb34f647a77ae43611dab3a447da447686352da5426baaff26c22a465dfe40c0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='b8c35301b56fde151b14e1bfb1374f579f5a0ed361d6ebc7ffff5f82eb563344';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='79fde4473b2c489278fdef105bf69097f1f1a0d54d75a59d24008773b512339b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f1989ee7f41d8d697e880dea74f94133841c2f59ded5c9dd551a26b87f4d36cf';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='eb1cd5b6bf532f10558e7067768d14884d9fce375d2782f91b2218365152bc42';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Oct 2022 14:21:59 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 05 Oct 2022 19:00:28 GMT
RUN apt-get update && apt-get install -y curl
# Wed, 05 Oct 2022 19:00:28 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 05 Oct 2022 19:00:29 GMT
ARG USER_HOME_DIR=/root
# Wed, 05 Oct 2022 19:00:30 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 05 Oct 2022 19:00:31 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 05 Oct 2022 19:00:39 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 05 Oct 2022 19:00:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 05 Oct 2022 19:00:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 05 Oct 2022 19:00:43 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 05 Oct 2022 19:00:44 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 05 Oct 2022 19:00:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 05 Oct 2022 19:00:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6d1a231d13b300fc73c20f074f3accd74dcff41afd006c272719fdf8cf9be075`  
		Last Modified: Tue, 04 Oct 2022 23:52:01 GMT  
		Size: 27.2 MB (27165243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766942147a0b9643dde5105adf200582201a20a0ef3ad86d7136e55632dd694c`  
		Last Modified: Wed, 05 Oct 2022 14:22:30 GMT  
		Size: 3.0 MB (2983220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a590bea68a831fcee3304072a3678ee2f07e2a7e0a23a0c1654611eba1d4b2f9`  
		Last Modified: Wed, 05 Oct 2022 14:23:20 GMT  
		Size: 154.5 MB (154503954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79e798495f24052b9b11512c2c068c38b130be8dce0abe1d4844d558dab8e16`  
		Last Modified: Wed, 05 Oct 2022 19:01:14 GMT  
		Size: 28.2 MB (28238823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a7738bcc9dfe8e39925fbd1c612a523e8ce89a2e78b6ea5e04896c3fd8239f`  
		Last Modified: Wed, 05 Oct 2022 19:01:12 GMT  
		Size: 8.7 MB (8739458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f8a0501d1c80462aa93b10ed040df82d4dd92effd87ce2f999ea858d905cfc`  
		Last Modified: Wed, 05 Oct 2022 19:01:11 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3918efaf66fa076adb229c08f05f59c1efb285ca9923313b6863470228918a0f`  
		Last Modified: Wed, 05 Oct 2022 19:01:11 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:9a99310bc28511a87278d85e59fda3945ef3a341e09780e730273e9967ac263b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.1 MB (234093699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5dfa026a5196cbdda324db24655a1b648a2cb5ff5c165150b56b8d830129f54`
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
# Wed, 28 Sep 2022 01:49:43 GMT
ENV JAVA_VERSION=8.0.7.16
# Wed, 28 Sep 2022 01:56:59 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb34f647a77ae43611dab3a447da447686352da5426baaff26c22a465dfe40c0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='b8c35301b56fde151b14e1bfb1374f579f5a0ed361d6ebc7ffff5f82eb563344';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='79fde4473b2c489278fdef105bf69097f1f1a0d54d75a59d24008773b512339b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f1989ee7f41d8d697e880dea74f94133841c2f59ded5c9dd551a26b87f4d36cf';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='eb1cd5b6bf532f10558e7067768d14884d9fce375d2782f91b2218365152bc42';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 28 Sep 2022 01:57:02 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 28 Sep 2022 03:23:51 GMT
RUN apt-get update && apt-get install -y curl
# Wed, 28 Sep 2022 03:23:52 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 28 Sep 2022 03:23:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 28 Sep 2022 03:23:53 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 28 Sep 2022 03:23:53 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 28 Sep 2022 03:23:55 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 28 Sep 2022 03:23:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 28 Sep 2022 03:23:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 28 Sep 2022 03:23:57 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 28 Sep 2022 03:23:57 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 28 Sep 2022 03:23:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 28 Sep 2022 03:23:58 GMT
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
	-	`sha256:d454df1776c1faf582a07577ff7ed25d8352b4e10e5a580a79397b515c3e663e`  
		Last Modified: Wed, 28 Sep 2022 01:58:51 GMT  
		Size: 166.3 MB (166285176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13862c4fb97a0a91895b529efe05ad6eca98a0d97e0beaac51cdc63f94a10e6e`  
		Last Modified: Wed, 28 Sep 2022 03:26:12 GMT  
		Size: 25.6 MB (25550125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb0a672a16508f8f369a191ae168ab609dae400b95264d18736f86c809cbbdfe`  
		Last Modified: Wed, 28 Sep 2022 03:26:09 GMT  
		Size: 8.7 MB (8739487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7b4c6af11d88d044e3f1278a6b9fddfc65f57dec1c2d32b408c1682ecc168b8`  
		Last Modified: Wed, 28 Sep 2022 03:26:08 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3d1b38755e31bb4a9a35533b8a1a60f2e3f3ff2c64a3a9e2d8b69796d30a3a`  
		Last Modified: Wed, 28 Sep 2022 03:26:08 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:8006dcd71f926e09c423bf187ef569451e2757c1c17818dcbc5da6f0b23d1571
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.1 MB (217073839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb960d41294dfce4f782696f7728489827efcd1999bbdc22dcb90f03597f72f0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 04 Oct 2022 23:52:31 GMT
ADD file:29c2a2a72a634a5f21c2f37cfd38da282528b75f75124d04e56a2f86f2e64121 in / 
# Tue, 04 Oct 2022 23:52:34 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 08:07:07 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Wed, 05 Oct 2022 08:07:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 08:07:26 GMT
ENV JAVA_VERSION=8.0.7.16
# Wed, 05 Oct 2022 08:10:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='bb34f647a77ae43611dab3a447da447686352da5426baaff26c22a465dfe40c0';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        i386)          ESUM='b8c35301b56fde151b14e1bfb1374f579f5a0ed361d6ebc7ffff5f82eb563344';          YML_FILE='8.0/sdk/linux/i386/index.yml';          ;;        ppc64el|ppc64le)          ESUM='79fde4473b2c489278fdef105bf69097f1f1a0d54d75a59d24008773b512339b';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390)          ESUM='f1989ee7f41d8d697e880dea74f94133841c2f59ded5c9dd551a26b87f4d36cf';          YML_FILE='8.0/sdk/linux/s390/index.yml';          ;;        s390x)          ESUM='eb1cd5b6bf532f10558e7067768d14884d9fce375d2782f91b2218365152bc42';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.bin ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.bin" | sha256sum -c -;     echo "INSTALLER_UI=silent" > /tmp/response.properties;     echo "USER_INSTALL_DIR=/opt/ibm/java" >> /tmp/response.properties;     echo "LICENSE_ACCEPTED=TRUE" >> /tmp/response.properties;     mkdir -p /opt/ibm;     chmod +x /tmp/ibm-java.bin;     /tmp/ibm-java.bin -i silent -f /tmp/response.properties;     rm -f /tmp/response.properties;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.bin;
# Wed, 05 Oct 2022 08:10:52 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Wed, 05 Oct 2022 17:41:04 GMT
RUN apt-get update && apt-get install -y curl
# Wed, 05 Oct 2022 17:41:05 GMT
ARG MAVEN_VERSION=3.8.6
# Wed, 05 Oct 2022 17:41:05 GMT
ARG USER_HOME_DIR=/root
# Wed, 05 Oct 2022 17:41:05 GMT
ARG SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26
# Wed, 05 Oct 2022 17:41:05 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries
# Wed, 05 Oct 2022 17:41:14 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.6/binaries MAVEN_VERSION=3.8.6 SHA=f790857f3b1f90ae8d16281f902c689e4f136ebe584aba45e4b1fa66c80cba826d3e0e52fdd04ed44b4c66f6d3fe3584a057c26dfcac544a60b301e6d0f91c26 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 05 Oct 2022 17:41:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 05 Oct 2022 17:41:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 05 Oct 2022 17:41:15 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 05 Oct 2022 17:41:15 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 05 Oct 2022 17:41:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 05 Oct 2022 17:41:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f41c9e2df5b8fcd28b58de30866b751466a2cbad7eb8f43e02d799439fb377cf`  
		Last Modified: Tue, 04 Oct 2022 23:54:09 GMT  
		Size: 25.4 MB (25370644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42b030bfbe7d3d22ba17686023d66542eece08a7b4916da1aa44dbd0fdc84f3`  
		Last Modified: Wed, 05 Oct 2022 08:11:26 GMT  
		Size: 2.7 MB (2671847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eecefa2f8f5a24ca441bfef6e86f26f96eb27ac714576f1f61fb33d8c2fa796c`  
		Last Modified: Wed, 05 Oct 2022 08:12:08 GMT  
		Size: 156.8 MB (156768693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74247f617c219ef4cf7f31c3bb8876f76ea30015beee698a411136a49f876ed`  
		Last Modified: Wed, 05 Oct 2022 17:44:32 GMT  
		Size: 23.5 MB (23521942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecf1557ad317932ec580bd5b3aa168afb38cc98b8542cc90425e8d56acbc93a`  
		Last Modified: Wed, 05 Oct 2022 17:44:30 GMT  
		Size: 8.7 MB (8739502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae4f7669c7690fffe1c32f3a6874e76aebd21ab3daf819ec75f89bdf145d7b2`  
		Last Modified: Wed, 05 Oct 2022 17:44:29 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911759fcb605278b6817af2be8ba2952d31ee82f191c0afe81335cae7ebb223d`  
		Last Modified: Wed, 05 Oct 2022 17:44:29 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
