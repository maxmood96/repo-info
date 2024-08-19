## `maven:3-eclipse-temurin-8`

```console
$ docker pull maven@sha256:8a112b5c500c6c3dde35d7c28646572126b8f16a88b3a9645046b81d249db26c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `maven:3-eclipse-temurin-8` - linux; amd64

```console
$ docker pull maven@sha256:0db6bee82730be63b74ea4234741e69c9fe4106b4072f0fa79858fbd6349e1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177872815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8460cc1f375864230be924b7d105bff78af7d6adab20c3512657b4413bdac42a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:c2e78eb585ec4e503f14c4ea98f4962c998f5eb075749507953f85387742694b in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 09:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:eb993dcd6942ffcb7633f2cb271bd4b0a275fc9bdc8f5100c5b4d24694cacf50`  
		Last Modified: Fri, 02 Aug 2024 03:03:23 GMT  
		Size: 30.6 MB (30567306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ad162d7203142bab0c47850dd2fcd205f950b3f9261ed4b68917cf906ca25a`  
		Last Modified: Sat, 17 Aug 2024 01:10:20 GMT  
		Size: 13.8 MB (13767059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7d83e556ca65db3b196e369c9761cc882b3b40405e74f459146a0ee800f3e05`  
		Last Modified: Sat, 17 Aug 2024 01:10:25 GMT  
		Size: 103.6 MB (103615827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85f71196939addb5eddef76a4bd7f5ce78ea71268a7a832d2aea24d0a355c60`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc5f3fec6046d26f916c03e180f06f455266f8a1332a1857d9f8d8daa621bc9`  
		Last Modified: Sat, 17 Aug 2024 01:10:17 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127564232de6a44a229e530e68bf3e0e0890f01cb0aeffe77e975e2e69b63bcf`  
		Last Modified: Sat, 17 Aug 2024 04:09:02 GMT  
		Size: 20.8 MB (20757782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bda4adaaa2b61c19f30a71c787fc7b57fa72f9ce749c2de518fd0bb6ea779f`  
		Last Modified: Sat, 17 Aug 2024 04:09:02 GMT  
		Size: 9.2 MB (9161811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcd3ef4c5efefa556ef66c839168c9f1e5795ad2349fa21fea824ea0da45d6b6`  
		Last Modified: Sat, 17 Aug 2024 04:09:02 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5338e19652a6b26088764875b7b5faa3f1ad36d42e0a29805e6ad4f06841953d`  
		Last Modified: Sat, 17 Aug 2024 04:09:02 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:e2f78ee40a8b53cea844cd95dc318f73e73d399e13d2bcfbf78fcab1a39c74bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4416684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7118d9b194c88d74d6a0940c7ac37b0c5199f774bac92fea7e0fdd042b892ed8`

```dockerfile
```

-	Layers:
	-	`sha256:04b5753d823588c673163cfad8a150ec274229f573b702546804b3456540449e`  
		Last Modified: Sat, 17 Aug 2024 04:09:02 GMT  
		Size: 4.4 MB (4397157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdf9f40ec4008fb83cbca3733abaf884d511b79f4fd9b6d0ad3b665dcdad09da`  
		Last Modified: Sat, 17 Aug 2024 04:09:02 GMT  
		Size: 19.5 KB (19527 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm variant v7

```console
$ docker pull maven@sha256:2b4dc77cd1a9129e720a35d0e17c76f5311afd977af908d99999c8ccfdf54af5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **174.9 MB (174865448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17557408297c6f1efb60a9596f6ed0282aa359cc613f667caad0ac456e5783f6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:7bcbd2cb56e3985e9aa22bb8b43873f12d7f999600db594761eaf685a9177b7e in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 09:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:dad4e753fc73fa87bcedddc090f436866b477fd660d61da6b81071b41ab85948`  
		Last Modified: Tue, 06 Aug 2024 02:06:08 GMT  
		Size: 27.7 MB (27689240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2daaa1493be2e58f55d0a68251ec270ec90fc978014e06ec0db5af0cbf608a44`  
		Last Modified: Sat, 17 Aug 2024 01:36:13 GMT  
		Size: 13.1 MB (13133360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ba04e85846682c2f7865889500fb94e58e943e24c5f8d9e05945669b190090f`  
		Last Modified: Sat, 17 Aug 2024 01:36:19 GMT  
		Size: 99.2 MB (99223915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:649b86a82cfedbeb1371e981cece7868f61c6734356b9de9bbbef151dbb7eefa`  
		Last Modified: Sat, 17 Aug 2024 01:36:10 GMT  
		Size: 128.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5b45a73dedc6ac57b88973dd794ed69ac2f20a32064454f4998e9bd9dadda6a`  
		Last Modified: Sat, 17 Aug 2024 01:36:11 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d3299bc7ba0cf9c8dcb6a518826583bc1e80bc7847eab18fbf246338c97a87`  
		Last Modified: Sat, 17 Aug 2024 04:41:04 GMT  
		Size: 25.7 MB (25654085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e535548d956cec538d733008b10f817038ffbeac8ddacec7611bcdedc90bb21`  
		Last Modified: Sat, 17 Aug 2024 04:41:03 GMT  
		Size: 9.2 MB (9161816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af4bdf81603eebbe702ac45289057078d33390817838e4ca67f9657bde83bec`  
		Last Modified: Sat, 17 Aug 2024 04:41:03 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee06992074f525fd63625c827eb4470dd22c7ab925ef407484adafb1ac196bb`  
		Last Modified: Sat, 17 Aug 2024 04:41:03 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:2f48275611cb442a6409c45e924b1abcf47d3f94f5abf23d4205a5d920b02ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4418236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a5989d134111d70b06826106f37f83a3d3f07b70cce3b0a7c7823272eec01a5`

```dockerfile
```

-	Layers:
	-	`sha256:c7e63d831a3cc3d187abac1d0fe7661a30fad445ea83791dee7d95e67f69adb2`  
		Last Modified: Sat, 17 Aug 2024 04:41:03 GMT  
		Size: 4.4 MB (4398601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9c8b0f7dc3bfc3e8e00eab665510cb9161e7ce7e24a87b6ef012e3c06a3d2246`  
		Last Modified: Sat, 17 Aug 2024 04:41:03 GMT  
		Size: 19.6 KB (19635 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4b311c8af80429c9c304b0645456edf3cfec62c00830cc9d9f970b1b2fa88faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **176.4 MB (176439888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad2a510e7bdedd65ecacd977a75b504e9a48c78d257c65417f696fe048cbe293`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
ARG RELEASE
# Thu, 27 Jun 2024 09:17:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:154285ca3d49a142bc6d59c9d48f14546f32b2d6de94387c30c1ba3759249b0f in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 09:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1567e7ea90b67fc95ccdeeec39bdc3045098dee7e0c604975b957a9f8c0e9616`  
		Last Modified: Fri, 02 Aug 2024 07:40:09 GMT  
		Size: 29.9 MB (29910029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:923b74992e2f6b4e4be4f1c2bf6930b93c7593d6c834159867d3bd8ea14005ff`  
		Last Modified: Sat, 17 Aug 2024 01:33:27 GMT  
		Size: 13.8 MB (13795899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58576ea718a0fe2438afe0bb666a3a35004198540087a002268e2962b41f7923`  
		Last Modified: Sat, 17 Aug 2024 01:33:31 GMT  
		Size: 102.7 MB (102732973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45b9a6c4f3c0f832785c77b255658197e74ce313e9fb3ee8cddfc9e630d56f59`  
		Last Modified: Sat, 17 Aug 2024 01:33:25 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd75ffbbc9e8eee9e198bb7d1025c93ea1d3b1669f3c950b9a5072d71f4e61c`  
		Last Modified: Sat, 17 Aug 2024 01:33:24 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b4ffd0c0307727e65a4257b50ecf7b2956bbb699946205decd413d65be0087`  
		Last Modified: Sat, 17 Aug 2024 12:04:38 GMT  
		Size: 20.8 MB (20836141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd25afb9059a573196b9bbdc430b0043682c32fc656b7bae6d960fef729d668`  
		Last Modified: Sat, 17 Aug 2024 12:04:37 GMT  
		Size: 9.2 MB (9161813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23a6d6d149cb9450976c75632a346d64bc5fd63b37a11fe8295d9eb729e81788`  
		Last Modified: Sat, 17 Aug 2024 12:04:36 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec36e5dc79cf1ded81dedeabcbd5621a60a417c5ef12c2b526dcbb7efa8e10c`  
		Last Modified: Sat, 17 Aug 2024 12:04:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:3a90b2bb661d82cb1d86ec612893b1a33236dcfeb1be417e7b3339c8712a4873
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.4 MB (4424450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b1a23de2888d8cd5ade7be20f7a00fde1cb5a09cc90c5967dd820e1b59bf889`

```dockerfile
```

-	Layers:
	-	`sha256:c6aef6df9e9392d4995646cede1b44482c3c116c3c2be8e44ee4413a384db089`  
		Last Modified: Sat, 17 Aug 2024 12:04:37 GMT  
		Size: 4.4 MB (4404285 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:237099011bd908a35bbcad5dfd2a6500df47d67df05766d1fea64dc17448a0e9`  
		Last Modified: Sat, 17 Aug 2024 12:04:36 GMT  
		Size: 20.2 KB (20165 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-8` - linux; ppc64le

```console
$ docker pull maven@sha256:09f2561714dbaf4a33d43f0c2ab1a93295fb8b3475e317db4b72b6b96ecac1a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **187.6 MB (187575678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac49665972162efec319fe73bb8e843361a13ca7f4229c55ec911bb5bdca64d5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Aug 2024 14:23:51 GMT
ARG RELEASE
# Thu, 01 Aug 2024 14:23:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 01 Aug 2024 14:23:51 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 01 Aug 2024 14:23:55 GMT
ADD file:f6dda5643c6c5671bba452213beef0fdd84c17bc5e733964b8b6d98a44d522a3 in / 
# Thu, 01 Aug 2024 14:23:55 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk8u422-b05
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='4c6056f6167fae73ace7c3080b78940be5c87d54f5b08894b3517eed1cbb2c06';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_x64_linux_hotspot_8u422b05.tar.gz';          ;;        arm64)          ESUM='af98a839ec238106078bd360af9e405dc6665c05ee837178ed13b92193681923';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_aarch64_linux_hotspot_8u422b05.tar.gz';          ;;        armhf)          ESUM='5bd0203b2b09b033e3a762299a4975939d7571b433eab8b59340cc966102bef1';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_arm_linux_hotspot_8u422b05.tar.gz';          apt-get update;          DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1;          rm -rf /var/lib/apt/lists/*;          ;;        ppc64el)          ESUM='78fbd7b01204cdf90bcb3f9fe6a8e9432bdaa75776fa333aa9cbcb5a79de34cd';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u422-b05/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u422b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     echo "javac -version"; javac -version;     echo "java -version"; java -version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git openssh-client --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6e87eba78bda982d63d6dcd89b529540108dd7b3549a594cdc780cc6e61b5b37`  
		Last Modified: Tue, 06 Aug 2024 02:06:20 GMT  
		Size: 35.6 MB (35627737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e370ad6ca2bf55a99908be5c652053972a6818bb55965d7aa787af36e351327d`  
		Last Modified: Sat, 17 Aug 2024 00:59:29 GMT  
		Size: 14.9 MB (14944549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3967ee3e86d8c475f87ea162f1d54dc6cfc8c951a262072bf24b6896e6e0c02`  
		Last Modified: Sat, 17 Aug 2024 00:59:39 GMT  
		Size: 101.1 MB (101079884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb134588d3539b9c607aa0125b5f2722bf3203f862406bcb03b15d2063c356c2`  
		Last Modified: Sat, 17 Aug 2024 00:59:25 GMT  
		Size: 127.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f31bdce3056ba85d1bfcd1ceb414f2f74b7218f645809332048dda6d2de4e2b`  
		Last Modified: Sat, 17 Aug 2024 00:59:25 GMT  
		Size: 1.9 KB (1867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9ddcdcf1e150ed3b57819b2837dc734e63242f6b50abcf212e09993464ac2a`  
		Last Modified: Mon, 19 Aug 2024 19:20:44 GMT  
		Size: 26.8 MB (26750031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247878889d4685426ba869d9f2a974ad6dfa72d1824d5d11952bdc0bcb06614a`  
		Last Modified: Mon, 19 Aug 2024 19:20:43 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bffcd16696a6e8ca4b4956edb755bd7912951e04725fcfeed99008d131ce423`  
		Last Modified: Mon, 19 Aug 2024 19:20:42 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c0620c41e8ac5abebfd50c64e12fff365c1293fc5daad337c87b5de077aa72b`  
		Last Modified: Mon, 19 Aug 2024 19:20:42 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-8` - unknown; unknown

```console
$ docker pull maven@sha256:cb3e85546776f0a052f1124c79410ada2863858a12618f7138e7e23afe0d0805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.5 MB (4481511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc5adb8c291bd5ff931b3c97532b912a8047d042db2a299b0e1284a39102e5c`

```dockerfile
```

-	Layers:
	-	`sha256:738603c7f13f1dc9bb0921bb15758daf1e7c9ff1b7b6487b1edf343e1f744b97`  
		Last Modified: Mon, 19 Aug 2024 19:20:42 GMT  
		Size: 4.5 MB (4461888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570d80685f0e54a78cd061af116394c2ebf6fb23ec7fe5eaedb3733d6ba1f0cf`  
		Last Modified: Mon, 19 Aug 2024 19:20:42 GMT  
		Size: 19.6 KB (19623 bytes)  
		MIME: application/vnd.in-toto+json
