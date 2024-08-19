## `maven:3-eclipse-temurin-17-focal`

```console
$ docker pull maven@sha256:dbab225e08f9a04f8adfe4ea2095d77dbf3527a9fca2b34071f07fa218d9c84c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `maven:3-eclipse-temurin-17-focal` - linux; amd64

```console
$ docker pull maven@sha256:1d709f8357680dd66c20457a11d99db0e618b8ececa27affa2707295425eee90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **231.9 MB (231931161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcd6bdc9e8f2456556129ab2aefee8400c6b156790c5f6124470409596014495`
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
LABEL org.opencontainers.image.version=20.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:e7cff353f027ecf0a2cb1cdd51714de3b083a11a0d965f104489f9a7e6925056 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 09:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["jshell"]
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
	-	`sha256:560c024910bebac6b404791af28ebd48a8289303b8377d17b67ffdfe52754f2a`  
		Last Modified: Mon, 03 Jun 2024 18:06:06 GMT  
		Size: 28.6 MB (28584223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5aedc0e1fdb7b1e0021df89491ab1ecb1d06f9ed9029843e236b44cc81d167`  
		Last Modified: Wed, 05 Jun 2024 05:00:16 GMT  
		Size: 20.7 MB (20672189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:460b26a845b3dacac3596a292cd7a4fc0b933f99c647ae88429fdb474e1b5705`  
		Last Modified: Tue, 23 Jul 2024 01:07:03 GMT  
		Size: 145.2 MB (145178336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01e3f73af39d0d03cfbec4869402d3c3b955717f2cc4c435e1a262c4769ce07e`  
		Last Modified: Tue, 23 Jul 2024 01:06:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882e4ba000be777c910ad7df6cabe1541d8b700cac349c035f8f481cece9ff42`  
		Last Modified: Thu, 25 Jul 2024 17:29:44 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c6d403eb4c990e319c7119496b467397a346620da945d6121c7398ea886b6b`  
		Last Modified: Sat, 17 Aug 2024 04:08:44 GMT  
		Size: 28.3 MB (28331511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d5961fa7c6d7ba878d43ada253c09ae238a450bcca462116237a7a59e4a112`  
		Last Modified: Sat, 17 Aug 2024 04:08:44 GMT  
		Size: 9.2 MB (9161817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7852c1ed13c330c788b206563dfb76ffbd12d07e672df242fec889916de03398`  
		Last Modified: Sat, 17 Aug 2024 04:08:43 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf547871f74eafd683da80f6f9d830a13f5e0ad6153a77e590a1f79dffaac29b`  
		Last Modified: Sat, 17 Aug 2024 04:08:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-focal` - unknown; unknown

```console
$ docker pull maven@sha256:83181c3d04070171476e7e2a4b77f7e784e5aaac8988ed031564632353e0b0d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5064679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73f2a05a67acdb2c5af7f6f4644732dc847cb78818104b003b6aa1a7f6b0d0da`

```dockerfile
```

-	Layers:
	-	`sha256:04f7bf67052347b639e64bac362ad6e57e1480b51f214de3f3ac008177a2d5dc`  
		Last Modified: Sat, 17 Aug 2024 04:08:44 GMT  
		Size: 5.0 MB (5045066 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b791ba7b83eb2b49e2eb8630583b18e566d004443184e39d1b826170ce1e474b`  
		Last Modified: Sat, 17 Aug 2024 04:08:43 GMT  
		Size: 19.6 KB (19613 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-focal` - linux; arm variant v7

```console
$ docker pull maven@sha256:24e36d999767c6b1364c8dbe164ed53a1c326bbf9f44ae7609d12db6498774ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221328048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f252ed9f8ef01b66aca4d92ce5e3501a54b372b2fd0c06f8991af519156f8420`
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
LABEL org.opencontainers.image.version=20.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:e8f5701e126fa109d02a19a62fdf05554cd10d627bb2a0a70238a8dc4ed63c77 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 09:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["jshell"]
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
	-	`sha256:fdbafd70c97f0cd921335e769caece4ff9a54483363cd205543860fb1e1cc94e`  
		Last Modified: Wed, 05 Jun 2024 03:30:49 GMT  
		Size: 24.6 MB (24603821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7727e8480ab0d546c03e272641ac75e49de4204e0ca2ce79b0c85c1b50fd9407`  
		Last Modified: Wed, 05 Jun 2024 04:01:52 GMT  
		Size: 20.0 MB (19957955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60a261ac4799d19425c98a8958ce356429a185b155daaa3ccd9c52c064bf9eff`  
		Last Modified: Tue, 23 Jul 2024 03:17:00 GMT  
		Size: 142.6 MB (142645314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303476b7ea40a2ba3c3fe0d37faa3537ff10fc69cfd923597b5a4ce4e098f697`  
		Last Modified: Tue, 23 Jul 2024 03:16:43 GMT  
		Size: 177.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144fdbcee19e83f636f34fc5fbbe7cada1b180bf75ca914e6b29e3e6b19afda3`  
		Last Modified: Thu, 25 Jul 2024 18:02:55 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d70858219686da1c6468db8fc3d9199e0268dd819f1925626f1478e37dba65`  
		Last Modified: Sat, 17 Aug 2024 04:40:23 GMT  
		Size: 25.0 MB (24956056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b97fffa09a129b6c21eb8259c266b655db85af1624f5ad55fc0d69af805baf`  
		Last Modified: Sat, 17 Aug 2024 04:40:23 GMT  
		Size: 9.2 MB (9161811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b7c4b5d87bdc060af25a2a52ad839595705cca050b0b7298133b55d62e4c88d`  
		Last Modified: Sat, 17 Aug 2024 04:40:22 GMT  
		Size: 861.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e09a9abe8f47ab0cb142da4e24150b5a63a6f3fbe143f5e36ea0f0a36fd3f47`  
		Last Modified: Sat, 17 Aug 2024 04:40:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-focal` - unknown; unknown

```console
$ docker pull maven@sha256:f9e80f48743627bba2826222768273c89bed1c8f4f1fcbfec79588356afaf92d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4984205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71075b2c7b15ed9ab4aba64c49aa93da233eb2bb0c090ccd3d1ac7c3482792ba`

```dockerfile
```

-	Layers:
	-	`sha256:4079aa208930b4ebb63109c1e06dd94668451bdbb37fafe19efeb114b561667c`  
		Last Modified: Sat, 17 Aug 2024 04:40:22 GMT  
		Size: 5.0 MB (4964465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed28eae05a8a9f1b57fcc25396096170abcc8222b648c7d00ad882ea031b7626`  
		Last Modified: Sat, 17 Aug 2024 04:40:22 GMT  
		Size: 19.7 KB (19740 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-focal` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2a9b5852ba9dd296ef009f5925d0c9900b4b04edf0386fcf22a196314f053cb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230068560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6a9be10092d5a3302729658fada7d7a217f359e52904d69fc62854b6769897`
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
LABEL org.opencontainers.image.version=20.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:6d8cc056ee741f09a6c7d965d8e2027d80ed2eccbfb0312593ce52d9256db437 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 27 Jun 2024 09:17:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["jshell"]
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
	-	`sha256:8cddf7b9c8a772efac198a7ae8bdfe15df2e065bb85f15cb8a223f6b3a2dbf9c`  
		Last Modified: Tue, 04 Jun 2024 16:08:03 GMT  
		Size: 27.2 MB (27205244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3947aac99c3e7c1d43015a496d42024cac8967a86cab89aef36ae800c0272bdd`  
		Last Modified: Wed, 05 Jun 2024 04:56:48 GMT  
		Size: 21.4 MB (21375371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:867b3de9f22fc9a80b614795706d0ab9b418935a0fc119bb4b08b2c3c09e0d0e`  
		Last Modified: Tue, 23 Jul 2024 04:12:42 GMT  
		Size: 144.0 MB (143967215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d51a74b88c1cc6131458a8bab48a7327f44645d9c1ed2e5ada16eed7c9eb376`  
		Last Modified: Tue, 23 Jul 2024 04:12:33 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccdcb7301dd518f5a07580bc653c44ecdbfc06a26ebc23e699e9da7b5a5213a`  
		Last Modified: Thu, 25 Jul 2024 17:45:41 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6174e390c9bdb7e49a1b68dac1114dc7278ccb1afda0f03935225bc9b5d00294`  
		Last Modified: Sat, 17 Aug 2024 12:00:20 GMT  
		Size: 28.4 MB (28355830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d441ed9baacaf27be6b00a37f14e2352d9fb4aac704e5b6d0c51cb654e905d5`  
		Last Modified: Sat, 17 Aug 2024 12:00:20 GMT  
		Size: 9.2 MB (9161815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2be170bc97edbbd1a6629e941c71be14c655a86731970acd0f54c5db7b20cda4`  
		Last Modified: Sat, 17 Aug 2024 12:00:19 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67aa0b743b4069fa4c70f4ff3da88a994b65237db467361893c624f6bcdc4008`  
		Last Modified: Sat, 17 Aug 2024 12:00:20 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-focal` - unknown; unknown

```console
$ docker pull maven@sha256:b3d324962a60b14a4aa8fa9a8ddbf3801ccf6ceafe1f05672b04b2a28f9cb4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881e3dba3501ff7ad3266ba7c1d428d6cb6e0cf407d758fa808f8010e86e7af1`

```dockerfile
```

-	Layers:
	-	`sha256:95778e8ee653796fd2adb2854229ced91bf02afcc61b0ed1df02494fd4aa0e89`  
		Last Modified: Sat, 17 Aug 2024 12:00:20 GMT  
		Size: 5.1 MB (5147279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7308c79fba3af51fbc9e6542763515d600260cb4f363e3b1f3a987bc38acd4d`  
		Last Modified: Sat, 17 Aug 2024 12:00:19 GMT  
		Size: 20.3 KB (20269 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-focal` - linux; ppc64le

```console
$ docker pull maven@sha256:6c3dccca1ee00cc061d2e972885199510366c4141bc8838341bf166d1563be21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.3 MB (247339091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:465a6d808afd48abd9a5d4aeee738a96759998335bd70d1541b0931711dee21b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Aug 2024 09:30:49 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:30:49 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:30:49 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:30:52 GMT
ADD file:7d009a6f6f630a25fba49573f13f6e4cdec238cb4420829b37d53d9a97b8a941 in / 
# Tue, 13 Aug 2024 09:30:52 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
CMD ["jshell"]
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
	-	`sha256:eb386e2cea8559613691083e515b5dad445536487242267707f4a8aec6a17286`  
		Last Modified: Wed, 05 Jun 2024 03:47:07 GMT  
		Size: 33.3 MB (33316120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7279313aa43260c90e56081f2f0fa3737f14cb0dce37ae46dc81d4ec4f561e1f`  
		Last Modified: Wed, 05 Jun 2024 04:02:27 GMT  
		Size: 22.7 MB (22715832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71a9f0efdba1b837a77b11e9c5274d8531a6731f0c76cfe5f2ae2252c69dc86`  
		Last Modified: Tue, 23 Jul 2024 01:42:34 GMT  
		Size: 144.9 MB (144864837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07bbaa65568bf9a4164ed7225cf03fb884535018c25b038d738f6efdb3308dc`  
		Last Modified: Tue, 23 Jul 2024 01:42:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3f306e16895da2965c7a50eb4c48a0d84ad2e08bc349ab244c7d7ed1d82ce7f`  
		Last Modified: Thu, 25 Jul 2024 17:24:49 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:559985b4444456f9350206dad5af01ca5d963afec88bc5d706f46ca62e1eeac7`  
		Last Modified: Mon, 19 Aug 2024 19:15:11 GMT  
		Size: 37.3 MB (37268773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bf3acb8a5b837f775b7ec286f25dce577ea5259494b28c226412ce83d163e10`  
		Last Modified: Mon, 19 Aug 2024 19:15:11 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b80b1989456afcdbf0a7279e7e5884bbd466b48b6a69783eea8264f3a59c2e1`  
		Last Modified: Mon, 19 Aug 2024 19:15:10 GMT  
		Size: 860.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa45c3f23495a2de2bcb79b5f5002f52160c17762b6f2a5e3511917a52fcc96`  
		Last Modified: Mon, 19 Aug 2024 19:15:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-focal` - unknown; unknown

```console
$ docker pull maven@sha256:61d5e5c2300ab23c6e362ba20ca293c2508297ab9f4b0469493de30c2f575dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5146149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90d0e65ca406a0d54f15d0b206a2ee322f92028c0ed2c01cbe1924b5e575fca9`

```dockerfile
```

-	Layers:
	-	`sha256:e4b27859749177b78caa15df7582fcc4b92e4d93e4bba846b80dc4a6cad7e97e`  
		Last Modified: Mon, 19 Aug 2024 19:15:10 GMT  
		Size: 5.1 MB (5126428 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8ce8690771be692b0aa1d440dcc4a2b3a1b517aa823e3ed7c255fe1960aefaf`  
		Last Modified: Mon, 19 Aug 2024 19:15:10 GMT  
		Size: 19.7 KB (19721 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-17-focal` - linux; s390x

```console
$ docker pull maven@sha256:e36c61d1079a165fabb35a77b7548e5193addab7f93cf8e32eb840f2d33bd701
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.6 MB (220624669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ac9911317dec9fc4852171e28dac94be345470ab2866d43c150bde5d4ccce3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 13 Aug 2024 09:29:15 GMT
ARG RELEASE
# Tue, 13 Aug 2024 09:29:15 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 13 Aug 2024 09:29:15 GMT
LABEL org.opencontainers.image.version=20.04
# Tue, 13 Aug 2024 09:29:17 GMT
ADD file:39767f0b13dc17d01020c3b8f88f8738a789fa7a5b27336e218ba44a42cbb60c in / 
# Tue, 13 Aug 2024 09:29:18 GMT
CMD ["/bin/bash"]
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jul 2024 22:19:06 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jul 2024 22:19:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='9d4dd339bf7e6a9dcba8347661603b74c61ab2a5083ae67bf76da6285da8a778';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_linux_hotspot_17.0.12_7.tar.gz';          ;;        arm64)          ESUM='8257de06bf37f0c8f19f8d542e2ab5a4e17db3ca5f29d041bd0b02ab265db021';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_aarch64_linux_hotspot_17.0.12_7.tar.gz';          ;;        armhf)          ESUM='ce7873ebf40ed0eb1089941ead4d3af79a205b1264f3162860d26ae957572b74';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_arm_linux_hotspot_17.0.12_7.tar.gz';          ;;        ppc64el)          ESUM='c97988e5a99b8ae0c47ba330b0883398c7433312db0051d8c5ff97911bae1605';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_ppc64le_linux_hotspot_17.0.12_7.tar.gz';          ;;        s390x)          ESUM='e244947f4c9176bd559598874b6ecaafcabba19c7067271cebb78708c2e9d14f';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_s390x_linux_hotspot_17.0.12_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Wed, 24 Jul 2024 22:19:06 GMT
ENTRYPOINT ["/bin/bash" "/__cacert_entrypoint.sh"]
# Wed, 24 Jul 2024 22:19:06 GMT
CMD ["jshell"]
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
	-	`sha256:ef41535c40f05e4212ae6933472799342ac3f01e687718bc7f1bb59e7eb40810`  
		Last Modified: Wed, 05 Jun 2024 03:12:18 GMT  
		Size: 27.0 MB (27013418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4616fbef706655b2aec3e9799581587b3d48a3bfca23b4984ec604fc5fba9135`  
		Last Modified: Wed, 05 Jun 2024 03:13:21 GMT  
		Size: 20.1 MB (20142321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0509cee5fbe81fbad90fc9f8fcd22d5d43e0dd5ad8811944795e2e163472d1b`  
		Last Modified: Tue, 23 Jul 2024 02:42:35 GMT  
		Size: 134.4 MB (134408626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a389f88882a2715261fb14b2fd7190d2782317e71d242f74c0802f230750e3d`  
		Last Modified: Tue, 23 Jul 2024 02:42:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f7bc8ab87210e8b75cf27163522859529d58291049af240193e02bbc68cbed6`  
		Last Modified: Thu, 25 Jul 2024 17:48:22 GMT  
		Size: 1.9 KB (1866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c36151cf9fe1e975e6543046ce094e97ad3c9d97f15b80fb919b966e758bf4c`  
		Last Modified: Mon, 19 Aug 2024 19:14:47 GMT  
		Size: 29.9 MB (29886775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37386cde8449eb51e52fcfba43f6dc4343c2961154dc2292087efcc80c7456ec`  
		Last Modified: Mon, 19 Aug 2024 19:14:47 GMT  
		Size: 9.2 MB (9170444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a76a58c2b5a5129fec0a51ba9754fddafd77319eb85c8a12dc3fadb5732c8dc`  
		Last Modified: Mon, 19 Aug 2024 19:14:47 GMT  
		Size: 859.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbb032899e097a4f77b5301be9e631583b6ac5b553b686fd6a1bf26656ee262a`  
		Last Modified: Mon, 19 Aug 2024 19:14:47 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-17-focal` - unknown; unknown

```console
$ docker pull maven@sha256:7be1f66a6d34e95ec080a4c63c18e9cdabaa7df877b40f4bd441150c86316283
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5040411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f48710f1bd96f3a3e5d696b3aecf843a0eb038eeef7fb4fe75438441831948`

```dockerfile
```

-	Layers:
	-	`sha256:167e3d72da174920955def0ec4f62836459dae434cc585407f4310940965c6fe`  
		Last Modified: Mon, 19 Aug 2024 19:14:47 GMT  
		Size: 5.0 MB (5020733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:313ec73c0be57f3a3f53aa390a05ef84aea5413b7f1c9ff06b8e8cc50d9c4c82`  
		Last Modified: Mon, 19 Aug 2024 19:14:46 GMT  
		Size: 19.7 KB (19678 bytes)  
		MIME: application/vnd.in-toto+json
