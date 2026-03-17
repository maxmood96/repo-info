## `maven:ibmjava`

```console
$ docker pull maven@sha256:65600f8401537e8e18a639395269d37937229cbba9adad7e776604d83f8bf54b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:ibmjava` - linux; amd64

```console
$ docker pull maven@sha256:015bf0fd960c9fd0baad710b56981599e71a97bdf1e4b11d2cb748a1484ade59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.5 MB (216473716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b669c4119cc633ceb14c88f690a4610b9dd9c78fc28a23087e9fb61ebd57c9c6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Feb 2026 07:30:06 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:30:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:30:06 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:30:08 GMT
ADD file:87202021c36509f80e5414aa2307ce867cd2e3b5f0d0f3bd0c98749793bd1fb4 in / 
# Tue, 24 Feb 2026 07:30:08 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 01:39:02 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 01:39:02 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:39:02 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 01:39:57 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 01:39:57 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 17 Mar 2026 03:44:44 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:44:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:44:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:44:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:44:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:44:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:44:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:44:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:44:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:44:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:44:45 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:44:45 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:44:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:44:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:44:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:96c832531c38e688c852576582a5ab43a21815c743665a03b6b066c850ed1522`  
		Last Modified: Tue, 24 Feb 2026 08:07:44 GMT  
		Size: 29.5 MB (29538520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486a0cc1bc5c4630c334e3ef2214d1ad765d760a43a7054dcbfade82afe29283`  
		Last Modified: Tue, 17 Mar 2026 01:40:14 GMT  
		Size: 1.5 MB (1450067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb898a25d9c64b330791cfa3f3d3639a8d6863cc4d6ffdcd61d7e5da57cd6dc9`  
		Last Modified: Tue, 17 Mar 2026 01:40:18 GMT  
		Size: 173.1 MB (173058228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37babece3196ba8795a1321afaa856a94e7d5b22ac95d06990b94268bea09770`  
		Last Modified: Tue, 17 Mar 2026 03:44:54 GMT  
		Size: 3.1 MB (3114687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c84f0f5d7fb710f75ffb0c1392dd331155e191e558032511b3ef6d937e64dd`  
		Last Modified: Tue, 17 Mar 2026 03:44:55 GMT  
		Size: 9.3 MB (9311178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c394ce7e173043f5b37cb8af23677c329a5efaa59786f70b9735e2353af1adec`  
		Last Modified: Tue, 17 Mar 2026 03:44:54 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ea5d80d72a3c6fc4e1e65ca83c10ece05b6fc361e6915ed92e0c3863d07f87`  
		Last Modified: Tue, 17 Mar 2026 03:44:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:15fb3414a4c97de41cac9e231f64812407373b23ae22da47b7977b91a1f99f57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3295635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d47bba874b41884a199c11429059d825a752b71e433527bb71135e660c72ab`

```dockerfile
```

-	Layers:
	-	`sha256:455e5c04cf39f23f7ae3cc17d4a0de3eaf52de93338f8b0dedc557fb8ef4ad99`  
		Last Modified: Tue, 17 Mar 2026 03:44:54 GMT  
		Size: 3.3 MB (3276857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71c4fd3647abce49e810414c2c81fc98213204690dcd1c25a073a7e4d7a527f6`  
		Last Modified: Tue, 17 Mar 2026 03:44:54 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; ppc64le

```console
$ docker pull maven@sha256:eaa4dfb788ae6dbb58d701d6f1d257f6a370f582cfb2abfe2741fbdf1c7aec64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.4 MB (223442440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12bf3568997f0121c5487fdc0e5a0b3cec64520b901330bc45dcdc29639fcb79`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Feb 2026 07:34:11 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:34:11 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:34:11 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:34:16 GMT
ADD file:8cdc5dcac981a23986a941c048f55a86d8ba46328e91ad30db9af43286781c61 in / 
# Tue, 24 Feb 2026 07:34:16 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 09:00:17 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 09:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 09:00:17 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 09:02:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 09:02:39 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 17 Mar 2026 22:05:13 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 22:05:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 22:05:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:05:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 22:05:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 22:05:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 22:05:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 22:05:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 22:05:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 22:05:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 22:05:20 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 22:05:20 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 22:05:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 22:05:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 22:05:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:31e4dc9ee1718c21d378c7cdb3929e157eabf4d70fe4bbe2e6b8ec5289e836dc`  
		Last Modified: Tue, 24 Feb 2026 08:08:05 GMT  
		Size: 34.5 MB (34453448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058d2f7f8365d8d5d5c83ad30e1c8995b2eaa6b1c50b7e1b1caa14e6ba0d13e1`  
		Last Modified: Tue, 17 Mar 2026 09:01:28 GMT  
		Size: 1.5 MB (1536093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c401a6ed6a34f2058c3b651c40d5634f706de4db2c5dd73a816a6e6481685f`  
		Last Modified: Tue, 17 Mar 2026 09:03:19 GMT  
		Size: 174.2 MB (174212709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba727117f54c9c4cf0ec3f0b8f88139df2df2122944256da926347cc54990513`  
		Last Modified: Tue, 17 Mar 2026 22:05:41 GMT  
		Size: 3.9 MB (3927979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d89ba853bed33c21729194421d056eb486686bc3dae2b577a578589b6b0c605`  
		Last Modified: Tue, 17 Mar 2026 22:05:41 GMT  
		Size: 9.3 MB (9311173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d0c9a30ccd4b2ccabe6a5f35356a9932bd6e4ea79da2952ae03675a7bcd267`  
		Last Modified: Tue, 17 Mar 2026 22:05:40 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:049bad7effbf9aaa036f60fe12976583d452f4a51d96ff6cdaeffe44926a8aeb`  
		Last Modified: Tue, 17 Mar 2026 22:05:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:12d4b4e9ef2223c02fecb6e95004480b7fa6f2ade1c011a7b618f6f7597a7fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 MB (3281820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28bd9d747a1cdf64d747aeaab95b0e9519fe44b08afc368d91bdfca56756eb8e`

```dockerfile
```

-	Layers:
	-	`sha256:021e3bd6f0115027108dd8422f8f5bf02f660fddf399ff00e6b392e191afc1ac`  
		Last Modified: Tue, 17 Mar 2026 22:05:41 GMT  
		Size: 3.3 MB (3262968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e8a9747c2c65e29ab5ea4a99db2094eaba3cc1d9c3e0e98602ba045001a9f7a6`  
		Last Modified: Tue, 17 Mar 2026 22:05:40 GMT  
		Size: 18.9 KB (18852 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:ibmjava` - linux; s390x

```console
$ docker pull maven@sha256:206f2e5bad505dac8206b15aae74ba572b6a5de698d2e5c0258e79d130caf15d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205462178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc2ec06756f60af601cd95546bfcb0397adb6a9f5eb736d7ec359aa96fecad47`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 24 Feb 2026 07:33:34 GMT
ARG RELEASE
# Tue, 24 Feb 2026 07:33:34 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 24 Feb 2026 07:33:35 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 24 Feb 2026 07:33:36 GMT
ADD file:03057d2fc9102d77c6c1ba39821174f9277c7aeb8de5358b12c437097e81cdb8 in / 
# Tue, 24 Feb 2026 07:33:36 GMT
CMD ["/bin/bash"]
# Tue, 17 Mar 2026 02:34:08 GMT
MAINTAINER Jayashree Gopi <jayasg12@in.ibm.com> (@jayasg12)
# Tue, 17 Mar 2026 02:34:08 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 02:34:08 GMT
ENV JAVA_VERSION=8.0.8.60
# Tue, 17 Mar 2026 02:35:36 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6f585e7ce294b9cbcd34a2f20344fa85a02be36ec777557eaf33da11b79ba5eb';          YML_FILE='8.0/sdk/linux/x86_64/index.yml';          ;;        ppc64el|ppc64le)          ESUM='bd63765ff2636772d86629f531a74260a6cc133e10c7cfd71ee730f2371c72a0';          YML_FILE='8.0/sdk/linux/ppc64le/index.yml';          ;;        s390x)          ESUM='20e371ae07354a41642c21fa6a84d88b384448b092fc725f95c4328ffa0c1bbd';          YML_FILE='8.0/sdk/linux/s390x/index.yml';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     BASE_URL="https://public.dhe.ibm.com/ibmdl/export/pub/systems/cloud/runtimes/java/meta/";     wget -q -U UA_IBM_JAVA_Docker -O /tmp/index.yml ${BASE_URL}/${YML_FILE};     JAVA_URL=$(sed -n '/^'${JAVA_VERSION}:'/{n;s/\s*uri:\s//p}'< /tmp/index.yml);     wget -q -U UA_IBM_JAVA_Docker -O /tmp/ibm-java.tgz ${JAVA_URL};     echo "${ESUM}  /tmp/ibm-java.tgz" | sha256sum -c -;     mkdir -p /opt/ibm/java;     tar -xf /tmp/ibm-java.tgz -C /opt/ibm/java --strip-components=1;     rm -f /tmp/index.yml;     rm -f /tmp/ibm-java.tgz; # buildkit
# Tue, 17 Mar 2026 02:35:36 GMT
ENV JAVA_HOME=/opt/ibm/java/jre PATH=/opt/ibm/java/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin IBM_JAVA_OPTIONS=-XX:+UseContainerSupport
# Tue, 17 Mar 2026 15:18:04 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 15:18:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 15:18:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 15:18:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 15:18:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 15:18:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 15:18:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 15:18:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 15:18:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 15:18:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 15:18:04 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 15:18:04 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 15:18:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 15:18:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 15:18:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b108e2a3f64e047295acfb714c51eedfbd4912d55d53e8bbbad5c2ac52fdf289`  
		Last Modified: Tue, 24 Feb 2026 08:08:19 GMT  
		Size: 28.0 MB (28007102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ec19658856db1b8624bd8ebec866bdd80a75f89b9975fa0a83c84c0a82533d`  
		Last Modified: Tue, 17 Mar 2026 02:35:34 GMT  
		Size: 1.5 MB (1455803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23bbc57d9e744b627543ae7ccf124d2070352c70ba38bb69f933a24bee3fbbe`  
		Last Modified: Tue, 17 Mar 2026 02:36:06 GMT  
		Size: 163.6 MB (163630508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:874ea90588aa39cfcef5a05db344ca9bed8e86e7a6b0984952bdbacbefac3c0d`  
		Last Modified: Tue, 17 Mar 2026 15:18:19 GMT  
		Size: 3.1 MB (3056544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16d56efd52ae8dea2068623e77c64994828873ff0a2d781bec964568b88f820`  
		Last Modified: Tue, 17 Mar 2026 15:18:19 GMT  
		Size: 9.3 MB (9311182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a54355c3aedfac67e5810f49e0fc65ef0cc1f6224c94ee19dc9f72bd4cb3b`  
		Last Modified: Tue, 17 Mar 2026 15:18:19 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b3fb2ad4a53fe3f34e9d20393a73fd5faa526b91d55e35ea1bc9d87a4c2277`  
		Last Modified: Tue, 17 Mar 2026 15:18:19 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:ibmjava` - unknown; unknown

```console
$ docker pull maven@sha256:4a1484c6dbcd23e814cfa7d804b617607a6f962fa572297377112c119bc6287d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2968935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dbeb9e76b20fe895735428c143a5889d9c0fd154f8468b964960f35ced5ee0e`

```dockerfile
```

-	Layers:
	-	`sha256:212132accd4dcd712fcf2f5cb3c50af3557ba348cc7297d3df05f6053e1ecbd2`  
		Last Modified: Tue, 17 Mar 2026 15:18:19 GMT  
		Size: 3.0 MB (2950157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ea5358358949db74d9034282895277e0fa9d82e4b1fdf56ffe3c471dc3923f9`  
		Last Modified: Tue, 17 Mar 2026 15:18:18 GMT  
		Size: 18.8 KB (18778 bytes)  
		MIME: application/vnd.in-toto+json
