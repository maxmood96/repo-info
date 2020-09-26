## `maven:adoptopenjdk`

```console
$ docker pull maven@sha256:a91051802898de3b3f0577c2e232e873e52491825e24c9ba4595b5bc206254fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `maven:adoptopenjdk` - linux; amd64

```console
$ docker pull maven@sha256:2ddb812ef6f99e19e44012d21dcbb577f3468528131c05f3fdecd011d87d2068
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.8 MB (291811150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f73797859920de3da0c750fa414ecd5b3feeda08223933ac5231af4790e98b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Sep 2020 22:20:02 GMT
ADD file:84f8ddc4d76e1e867ab084f300cf4c2397bb9e4628d83dc22f4f5e2f6ec670b4 in / 
# Wed, 16 Sep 2020 22:20:03 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 22:20:04 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 22:20:05 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 22:20:05 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:34:43 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Sep 2020 23:35:09 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:37:23 GMT
ENV JAVA_VERSION=jdk-14.0.2+12
# Wed, 16 Sep 2020 23:37:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ee87e9f03b1fbe6f328429b78fe1a9f44900026d220c90dfd747fe0bcd62d904';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_aarch64_linux_hotspot_14.0.2_12.tar.gz';          ;;        armhf|armv7l)          ESUM='65f193496c6977ba7aed1563edc4b5be091b5ff03e3d790074bb4e389a034b36';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_arm_linux_hotspot_14.0.2_12.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='465a3b8e931896b8d95e452d479615c4bf543535c05b6ea246323ae114e67d7d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_ppc64le_linux_hotspot_14.0.2_12.tar.gz';          ;;        s390x)          ESUM='7d27aea30e359cf0bb561f8dcca6f4591dbc3ae831981f8a19aa367d31a9709b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_s390x_linux_hotspot_14.0.2_12.tar.gz';          ;;        amd64|x86_64)          ESUM='7d5ee7e06909b8a99c0d029f512f67b092597aa5b0e78c109bd59405bbfa74fe';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_x64_linux_hotspot_14.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 16 Sep 2020 23:37:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Sep 2020 23:37:41 GMT
CMD ["jshell"]
# Thu, 17 Sep 2020 04:05:28 GMT
ARG MAVEN_VERSION=3.6.3
# Thu, 17 Sep 2020 04:05:28 GMT
ARG USER_HOME_DIR=/root
# Thu, 17 Sep 2020 04:05:28 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Thu, 17 Sep 2020 04:05:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Thu, 17 Sep 2020 04:05:37 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 04:05:39 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 17 Sep 2020 04:05:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 17 Sep 2020 04:05:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 17 Sep 2020 04:05:40 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 17 Sep 2020 04:05:40 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 17 Sep 2020 04:05:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 17 Sep 2020 04:05:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5d9821c948472065b3c166b4abc08367160961c9ac4639eb0023670ab4845a6a`  
		Last Modified: Fri, 04 Sep 2020 12:21:34 GMT  
		Size: 26.7 MB (26699608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a610eae58dfceafc0725cb0472249020f75bcc796468615798ee394cbaf86120`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40e0eb9f1408cd0bee02979b33f05689110bc9caba370388d94f73b46a6379a`  
		Last Modified: Wed, 16 Sep 2020 22:23:01 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1854bb447e96b1e5e1051bef627b6167e587e689da45e38caada1a12fd195061`  
		Last Modified: Wed, 16 Sep 2020 23:41:46 GMT  
		Size: 13.9 MB (13875245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5777b740e9890f8b7114a340703724bd3aa151e42a9f4d26589cd13d009f58`  
		Last Modified: Wed, 16 Sep 2020 23:44:02 GMT  
		Size: 211.8 MB (211806971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbae12033127b8ce42a13ed7e218960c54082af1bfd8a6845ee12554046c047`  
		Last Modified: Thu, 17 Sep 2020 04:08:08 GMT  
		Size: 29.8 MB (29845884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bba3a04d036d3625228317ebdc4f0ca40e4d40c3dddd5eb100dcc3d3a77a255`  
		Last Modified: Thu, 17 Sep 2020 04:08:03 GMT  
		Size: 9.6 MB (9581217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd7a89da8439b4e96ec276fc8b9b86f88bdd12b95eb8a0700d312f491b8f48fc`  
		Last Modified: Thu, 17 Sep 2020 04:08:03 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e62765c84bb842c92de15086a0888fd2fd15d1d6a85258b1dffdded53a56b7`  
		Last Modified: Thu, 17 Sep 2020 04:08:03 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:adoptopenjdk` - linux; arm variant v7

```console
$ docker pull maven@sha256:0e187985c79ebb248f41da30415f2c9e6278a58dfe4f2d23adc868afea1b43e2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268530090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632ab5f7d1a2f7c6fb6489ae0571996aa88f220fddc598ae307e204b3a73dbee`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 19 Aug 2020 21:45:03 GMT
ADD file:8369fef9339cb0f1b2b9660d860a6cbf4a5cd6c5e173fbb8cdf8b9485e56aaf4 in / 
# Wed, 19 Aug 2020 21:45:08 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 19 Aug 2020 21:45:10 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 19 Aug 2020 21:45:12 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 19 Aug 2020 21:45:12 GMT
CMD ["/bin/bash"]
# Wed, 19 Aug 2020 22:12:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 19 Aug 2020 22:12:37 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 19 Aug 2020 22:15:18 GMT
ENV JAVA_VERSION=jdk-14.0.2+12
# Wed, 19 Aug 2020 22:15:40 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ee87e9f03b1fbe6f328429b78fe1a9f44900026d220c90dfd747fe0bcd62d904';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_aarch64_linux_hotspot_14.0.2_12.tar.gz';          ;;        armhf|armv7l)          ESUM='65f193496c6977ba7aed1563edc4b5be091b5ff03e3d790074bb4e389a034b36';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_arm_linux_hotspot_14.0.2_12.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='465a3b8e931896b8d95e452d479615c4bf543535c05b6ea246323ae114e67d7d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_ppc64le_linux_hotspot_14.0.2_12.tar.gz';          ;;        s390x)          ESUM='7d27aea30e359cf0bb561f8dcca6f4591dbc3ae831981f8a19aa367d31a9709b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_s390x_linux_hotspot_14.0.2_12.tar.gz';          ;;        amd64|x86_64)          ESUM='7d5ee7e06909b8a99c0d029f512f67b092597aa5b0e78c109bd59405bbfa74fe';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_x64_linux_hotspot_14.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 19 Aug 2020 22:15:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Aug 2020 22:15:43 GMT
CMD ["jshell"]
# Thu, 20 Aug 2020 00:11:47 GMT
ARG MAVEN_VERSION=3.6.3
# Thu, 20 Aug 2020 00:11:53 GMT
ARG USER_HOME_DIR=/root
# Thu, 20 Aug 2020 00:12:00 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Thu, 20 Aug 2020 00:12:08 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Thu, 20 Aug 2020 00:12:54 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Thu, 20 Aug 2020 00:13:30 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 20 Aug 2020 00:13:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 20 Aug 2020 00:13:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 20 Aug 2020 00:13:59 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 20 Aug 2020 00:14:10 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 20 Aug 2020 00:14:16 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 20 Aug 2020 00:14:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:854ab59e811f2c269687884c4899a5de08a5f65b6489dffdb58754086f21e5fc`  
		Last Modified: Mon, 10 Aug 2020 14:29:24 GMT  
		Size: 22.3 MB (22278969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:996b7ca18b137080bed3caae4f18c24a2ae9b41a0bd9279d21fe013600e6dbf6`  
		Last Modified: Wed, 19 Aug 2020 21:47:13 GMT  
		Size: 35.5 KB (35458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a08dcf8afcac65e6356d202299b593954a299f9ebdb2db237496025225c8f2`  
		Last Modified: Wed, 19 Aug 2020 21:47:13 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34a2e7cb38ebbe96765deedfead50764f5a482a67ca440de7e9e660db464be7`  
		Last Modified: Wed, 19 Aug 2020 21:47:13 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c28a13f2c101b3996378f0c6d3848c55be63363f19fe99971b36de537e7d8b`  
		Last Modified: Wed, 19 Aug 2020 22:16:32 GMT  
		Size: 12.8 MB (12817129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03be241e4924eb9dc045924c213258aa2773bcb9a8e1a3d153f24810e75ae3f7`  
		Last Modified: Wed, 19 Aug 2020 22:19:38 GMT  
		Size: 198.0 MB (198004349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9081d17dafa5489b7934b55314587768e35f52025b2d132a57071f6f2b35f63`  
		Last Modified: Thu, 20 Aug 2020 00:18:14 GMT  
		Size: 25.8 MB (25810726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177b8bd8c3017fdd9a172b9391982a891d4f5dec76d3eac0d015496c7f92a261`  
		Last Modified: Thu, 20 Aug 2020 00:18:07 GMT  
		Size: 9.6 MB (9581198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd649c64b898db6a2b95d45518021e09b0d1b46d2a9b1489f128a57afafc384d`  
		Last Modified: Thu, 20 Aug 2020 00:18:06 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792b6f10d3fba91ec2af61c62315d6a8af4d59185d92905e618daacfbdd1e036`  
		Last Modified: Thu, 20 Aug 2020 00:18:06 GMT  
		Size: 367.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:adoptopenjdk` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fc36ab782832906b59c074ac8b47ba1bc54a639439fb699bb8f549aaf535be9e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.8 MB (283833783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bada842b947b40234ac8065fb61cdd2720bd4f59c61644b15b547e7554f4093d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Sep 2020 23:16:37 GMT
ADD file:9eedc88c2028d53a81210b52c98121dddea7e30ecfbd4d11d2a1b2bdc94a0102 in / 
# Wed, 16 Sep 2020 23:16:39 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:16:41 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:16:43 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:16:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Sep 2020 23:25:40 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 16 Sep 2020 23:26:07 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 16 Sep 2020 23:28:18 GMT
ENV JAVA_VERSION=jdk-14.0.2+12
# Wed, 16 Sep 2020 23:28:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ee87e9f03b1fbe6f328429b78fe1a9f44900026d220c90dfd747fe0bcd62d904';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_aarch64_linux_hotspot_14.0.2_12.tar.gz';          ;;        armhf|armv7l)          ESUM='65f193496c6977ba7aed1563edc4b5be091b5ff03e3d790074bb4e389a034b36';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_arm_linux_hotspot_14.0.2_12.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='465a3b8e931896b8d95e452d479615c4bf543535c05b6ea246323ae114e67d7d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_ppc64le_linux_hotspot_14.0.2_12.tar.gz';          ;;        s390x)          ESUM='7d27aea30e359cf0bb561f8dcca6f4591dbc3ae831981f8a19aa367d31a9709b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_s390x_linux_hotspot_14.0.2_12.tar.gz';          ;;        amd64|x86_64)          ESUM='7d5ee7e06909b8a99c0d029f512f67b092597aa5b0e78c109bd59405bbfa74fe';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_x64_linux_hotspot_14.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 16 Sep 2020 23:28:33 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 16 Sep 2020 23:28:34 GMT
CMD ["jshell"]
# Fri, 18 Sep 2020 02:39:17 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 18 Sep 2020 02:39:18 GMT
ARG USER_HOME_DIR=/root
# Fri, 18 Sep 2020 02:39:18 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 18 Sep 2020 02:39:19 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 18 Sep 2020 02:39:38 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Fri, 18 Sep 2020 02:39:44 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 18 Sep 2020 02:39:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 18 Sep 2020 02:39:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 18 Sep 2020 02:39:49 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 18 Sep 2020 02:39:50 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 18 Sep 2020 02:39:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 18 Sep 2020 02:39:51 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:e2d8ee3976bc7c15c8a5279cdf0249b7e41b2a489771330d0f7affb26dd7acfb`  
		Last Modified: Fri, 04 Sep 2020 00:25:25 GMT  
		Size: 23.7 MB (23722305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5007857f7b9b52d6efdfea9e086e6eaf35519130ff97bfe89970353f0ae53f13`  
		Last Modified: Wed, 16 Sep 2020 23:18:23 GMT  
		Size: 848.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43927e60f12d8b877ded6af5048b2ac5753fe78caba77a6bbbece4f98559b672`  
		Last Modified: Wed, 16 Sep 2020 23:18:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349d5fbbdf46d60d5864e631278bb555a928a5b16e534b20cd8b72e4671fce7b`  
		Last Modified: Wed, 16 Sep 2020 23:29:27 GMT  
		Size: 13.3 MB (13284762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d73eb42229ee952d87676e51ee627f22d1395aca6e6d9a1e8e35488d9f4f258a`  
		Last Modified: Wed, 16 Sep 2020 23:32:43 GMT  
		Size: 209.2 MB (209228565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:811f8055c22482f30196d69d6f1673831111668b05aa375288b29736ec533cca`  
		Last Modified: Fri, 18 Sep 2020 02:42:18 GMT  
		Size: 28.0 MB (28014705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d5fc3b6f6f14930fbdaf4bedf75be376694abb9e7f390df94f37137e0a62ab`  
		Last Modified: Fri, 18 Sep 2020 02:42:12 GMT  
		Size: 9.6 MB (9581201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da801f9f72fffe9db3ff942fd0029c285d752009d0ad96861c3598e7c81d190c`  
		Last Modified: Fri, 18 Sep 2020 02:42:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f77994ffe2c9bb4277d4b3acb359f15089d36ed62c6a01f4cccbebc776262a7`  
		Last Modified: Fri, 18 Sep 2020 02:42:10 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:adoptopenjdk` - linux; ppc64le

```console
$ docker pull maven@sha256:39be07a4de2a43bd5d7797552011a40ba095e0019571174fe083665a197062aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.4 MB (285380963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2413233c60c44c8fe0edae04651b9a7927d397affd1ee3c36b31fffd3a56378f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Sep 2020 23:54:24 GMT
ADD file:8f9c69dc1466e3fa3f47ef42daa366ad93d6a34e816768fb8dd35e541e61b9af in / 
# Wed, 16 Sep 2020 23:54:44 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Wed, 16 Sep 2020 23:54:54 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Wed, 16 Sep 2020 23:55:02 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Wed, 16 Sep 2020 23:55:04 GMT
CMD ["/bin/bash"]
# Thu, 17 Sep 2020 00:08:23 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Sep 2020 00:09:53 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 00:16:16 GMT
ENV JAVA_VERSION=jdk-14.0.2+12
# Thu, 17 Sep 2020 00:16:42 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ee87e9f03b1fbe6f328429b78fe1a9f44900026d220c90dfd747fe0bcd62d904';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_aarch64_linux_hotspot_14.0.2_12.tar.gz';          ;;        armhf|armv7l)          ESUM='65f193496c6977ba7aed1563edc4b5be091b5ff03e3d790074bb4e389a034b36';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_arm_linux_hotspot_14.0.2_12.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='465a3b8e931896b8d95e452d479615c4bf543535c05b6ea246323ae114e67d7d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_ppc64le_linux_hotspot_14.0.2_12.tar.gz';          ;;        s390x)          ESUM='7d27aea30e359cf0bb561f8dcca6f4591dbc3ae831981f8a19aa367d31a9709b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_s390x_linux_hotspot_14.0.2_12.tar.gz';          ;;        amd64|x86_64)          ESUM='7d5ee7e06909b8a99c0d029f512f67b092597aa5b0e78c109bd59405bbfa74fe';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_x64_linux_hotspot_14.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Sep 2020 00:16:51 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Sep 2020 00:16:54 GMT
CMD ["jshell"]
# Thu, 17 Sep 2020 04:48:13 GMT
ARG MAVEN_VERSION=3.6.3
# Thu, 17 Sep 2020 04:48:16 GMT
ARG USER_HOME_DIR=/root
# Thu, 17 Sep 2020 04:48:18 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Thu, 17 Sep 2020 04:48:20 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Thu, 17 Sep 2020 04:49:10 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Thu, 17 Sep 2020 04:49:20 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Thu, 17 Sep 2020 04:49:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 17 Sep 2020 04:49:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 17 Sep 2020 04:49:38 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Thu, 17 Sep 2020 04:49:39 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Thu, 17 Sep 2020 04:49:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 17 Sep 2020 04:49:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cab4317aedcc40ff2a2f72b253d06e717095a7e3cf1c28ab1ede6b2ee2113c28`  
		Last Modified: Mon, 07 Sep 2020 15:50:42 GMT  
		Size: 30.4 MB (30407200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62ab144e14fcd18dc307805290e556f638df374f6647d94816e4aa11f2c014a`  
		Last Modified: Thu, 17 Sep 2020 00:01:25 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ab01c61d5c7930829a28ce67f84f50f322fbb587f8c867af94413ae163e19c`  
		Last Modified: Thu, 17 Sep 2020 00:01:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9979d7fedd70abf0a194bac264009b81e45db4df709a1facde8ae8ab2efdf0ba`  
		Last Modified: Thu, 17 Sep 2020 00:25:41 GMT  
		Size: 14.5 MB (14518581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c7703194a7edf9a45bb9c1b2267c35d74762382dd0b754fbe7a1fdcdb11cbd`  
		Last Modified: Thu, 17 Sep 2020 00:28:59 GMT  
		Size: 193.6 MB (193561513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39c8960305f2b9350986f808d28e6ed1f7f4f29cd78635b042b9120ac8424e6e`  
		Last Modified: Thu, 17 Sep 2020 04:56:21 GMT  
		Size: 37.3 MB (37310224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa790f82f97a96636c3cb9286308e39bfe0989d6238d494fa917f76733fd99e`  
		Last Modified: Thu, 17 Sep 2020 04:56:15 GMT  
		Size: 9.6 MB (9581194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33842f657a7b585dd630e11b29961e9e94065ef4b6d10307d5f6e27539c856a2`  
		Last Modified: Thu, 17 Sep 2020 04:56:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c92b95264f612a4b5d842c22bdc3c47b5cdd5edee596ef06b51ac1fef862092`  
		Last Modified: Thu, 17 Sep 2020 04:56:13 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:adoptopenjdk` - linux; s390x

```console
$ docker pull maven@sha256:785f181277b72bfbe828d1815ed5640dfdfa344dbc87c920420ddd04956cd2d0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.6 MB (262573611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34b00f86a9ed7d20469cdb9e88c40581c201af2405e9603004fe3577c35e2960`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 25 Sep 2020 22:44:45 GMT
ADD file:0a8ec4fb62616b6605197e20e0a7b511dc5b03d4af0e04c929dfd9fb457d2065 in / 
# Fri, 25 Sep 2020 22:44:47 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 25 Sep 2020 22:44:48 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 25 Sep 2020 22:44:48 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 25 Sep 2020 22:44:48 GMT
CMD ["/bin/bash"]
# Fri, 25 Sep 2020 23:07:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 25 Sep 2020 23:07:34 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:09:23 GMT
ENV JAVA_VERSION=jdk-14.0.2+12
# Fri, 25 Sep 2020 23:09:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ee87e9f03b1fbe6f328429b78fe1a9f44900026d220c90dfd747fe0bcd62d904';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_aarch64_linux_hotspot_14.0.2_12.tar.gz';          ;;        armhf|armv7l)          ESUM='65f193496c6977ba7aed1563edc4b5be091b5ff03e3d790074bb4e389a034b36';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_arm_linux_hotspot_14.0.2_12.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='465a3b8e931896b8d95e452d479615c4bf543535c05b6ea246323ae114e67d7d';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_ppc64le_linux_hotspot_14.0.2_12.tar.gz';          ;;        s390x)          ESUM='7d27aea30e359cf0bb561f8dcca6f4591dbc3ae831981f8a19aa367d31a9709b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_s390x_linux_hotspot_14.0.2_12.tar.gz';          ;;        amd64|x86_64)          ESUM='7d5ee7e06909b8a99c0d029f512f67b092597aa5b0e78c109bd59405bbfa74fe';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jdk_x64_linux_hotspot_14.0.2_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 25 Sep 2020 23:09:42 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 25 Sep 2020 23:09:42 GMT
CMD ["jshell"]
# Fri, 25 Sep 2020 23:37:27 GMT
ARG MAVEN_VERSION=3.6.3
# Fri, 25 Sep 2020 23:37:27 GMT
ARG USER_HOME_DIR=/root
# Fri, 25 Sep 2020 23:37:27 GMT
ARG SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0
# Fri, 25 Sep 2020 23:37:28 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries
# Fri, 25 Sep 2020 23:37:37 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN apt-get update     && apt-get install -y git     && rm -rf /var/lib/apt/lists/*
# Fri, 25 Sep 2020 23:37:49 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.6.3/binaries MAVEN_VERSION=3.6.3 SHA=c35a1803a6e70a126e80b2b3ae33eed961f83ed74d18fcd16909b2d44d7dada3203f1ffe726c17ef8dcca2dcaa9fca676987befeadc9b9f759967a8cb77181c0 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 25 Sep 2020 23:37:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 25 Sep 2020 23:37:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 25 Sep 2020 23:37:50 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 25 Sep 2020 23:37:50 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 25 Sep 2020 23:37:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 25 Sep 2020 23:37:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:dd2de95b9a1c45e92bcc791d469201229b58d68187c99de6b08b00a13fa33393`  
		Last Modified: Fri, 25 Sep 2020 22:45:52 GMT  
		Size: 25.4 MB (25371975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38a48ef4dfab2bd639d381d11b3390b6bf8860b2ef3356e9bb55f7cb8c775f9`  
		Last Modified: Fri, 25 Sep 2020 22:45:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eced51184728468b347a6e3f143c356cd174c4a54be3cc10ec5aeddb402765fd`  
		Last Modified: Fri, 25 Sep 2020 22:45:49 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eb688908dd55f188cb3c2b3bb83efc30566ace847ab51ba28adbed5d30266b`  
		Last Modified: Fri, 25 Sep 2020 23:12:47 GMT  
		Size: 13.6 MB (13595725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dbebe4c79854ff35ca29c505378784938680b25d6081ca941489db884e44197`  
		Last Modified: Fri, 25 Sep 2020 23:14:32 GMT  
		Size: 184.5 MB (184530593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20488dbc33f3642d10bc6af772238ec5fa7b2fa355fc0bcf3fab3a2157ba8967`  
		Last Modified: Fri, 25 Sep 2020 23:40:01 GMT  
		Size: 29.5 MB (29491872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:428619aebe3eea57d0ba7b987c7b5e6ea42825911bcc43143cbfdae36efd0320`  
		Last Modified: Fri, 25 Sep 2020 23:39:57 GMT  
		Size: 9.6 MB (9581196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36083f1ec2d5527dafdfa22f50b180447293c9deb446451f393f35546d0b5c80`  
		Last Modified: Fri, 25 Sep 2020 23:39:57 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72096ea18188feab16175e9c57d80df305cbf00527f2d483ea0b0066b93257d`  
		Last Modified: Fri, 25 Sep 2020 23:39:57 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
