## `maven:3-eclipse-temurin-11`

```console
$ docker pull maven@sha256:e01fae5dea5352a794a106263ca5355f40e694fe872212a6ead1c2dc2ce2ca28
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

### `maven:3-eclipse-temurin-11` - linux; amd64

```console
$ docker pull maven@sha256:e8079e8ffec170ca003961f03f4a7620eba6eac7e59c7c7ea591a7e82e0f52aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.7 MB (216746578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f8bf9434498ef21758874c4595e1c91f8156a257d73d0bb9a42d4be868bbf7`
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
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708ff3b02f8b7b7711302f65e71cb2abbb60946f996f61dec11ce5788fc08f11`  
		Last Modified: Tue, 02 Jul 2024 06:00:37 GMT  
		Size: 12.9 MB (12871067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a651251312232415fd3dc5d41d293e3d622902907d26d7080406dfd83aebe839`  
		Last Modified: Tue, 02 Jul 2024 06:01:22 GMT  
		Size: 145.5 MB (145509443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f495773dd39114ecaa870dc3aaea7d8db9b3658bea759598e7f1b0c4201e0667`  
		Last Modified: Tue, 02 Jul 2024 06:01:10 GMT  
		Size: 176.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9473ee3b03a21d80d1e977a2a0f8e83665d1cad0de5a45183e9bc0b2eb396dbc`  
		Last Modified: Tue, 02 Jul 2024 06:01:10 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990b9f79dc2c9fd0ea376e64984f801c234a7ff68b535d7a43707aa0b8facff3`  
		Last Modified: Tue, 02 Jul 2024 07:11:10 GMT  
		Size: 18.8 MB (18762342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e26d536990a033b1e760e6380fbcc3d9129809f5fa3ffcc26e62cb044c5b544b`  
		Last Modified: Tue, 02 Jul 2024 07:11:10 GMT  
		Size: 9.2 MB (9161586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148707f8f49636febabdf62be5994a8eade45926bea154773e5df8de82b3f514`  
		Last Modified: Tue, 02 Jul 2024 07:11:10 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcf743d8e93cbff930522e13b564c7b990daf7a79e8ca1bfa10eb7792112832`  
		Last Modified: Tue, 02 Jul 2024 07:11:10 GMT  
		Size: 361.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e67e8b9d075cb688e9f4e550b848d26217046e42807daa5b31846921b93dac4`  
		Last Modified: Tue, 02 Jul 2024 07:11:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11` - unknown; unknown

```console
$ docker pull maven@sha256:1ccec06fed42c67ee8aec702835449eed5dd92723cc4b2b208127f35f1c5968b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4897030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38311201ab32ce553f8c5e7e424becf53d03fc8a12065893919cfe3939760a63`

```dockerfile
```

-	Layers:
	-	`sha256:b933dd4d13b5cdf1d1d37b9c4d34028c91794dc8f45af7c68ab97c8497f06456`  
		Last Modified: Tue, 02 Jul 2024 07:11:10 GMT  
		Size: 4.9 MB (4872649 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5aaffe3db2bb42c66543cfb0ea34ec739108054a207a03afc783efca1e8a38`  
		Last Modified: Tue, 02 Jul 2024 07:11:10 GMT  
		Size: 24.4 KB (24381 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-11` - linux; arm variant v7

```console
$ docker pull maven@sha256:f0bdd6dc7a1076db917ce1eb5cd484721a0421488c791fd48f12df40525689f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **209.2 MB (209232693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee0b2816acde3c4d0826ff46483b8136e9b64a9d6a28657c2a7105e4dd5c450`
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
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:967120bb21c0fbaf9bf6c8fcb7b292d31ec4812e538714e8beb0a6e013eae873 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:e180e7b68e21ed1490bb8293a3e848136812456d07f1be0783ef04f773a97867`  
		Last Modified: Fri, 28 Jun 2024 02:10:28 GMT  
		Size: 27.5 MB (27534011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3600b7820ccdab844af0b11c36a1aeadc460c5a3bc6a6fd0211a3fa9024fb1`  
		Last Modified: Tue, 02 Jul 2024 04:32:24 GMT  
		Size: 12.5 MB (12462968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5683275978575be7df9d26c3ae87f4576b2d810ec10b569c7331167fb751a9c`  
		Last Modified: Tue, 02 Jul 2024 04:33:37 GMT  
		Size: 138.0 MB (138004562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee4e9957dbca99a8013bcf78bffbe5eba97801c1181113196b1dc286d813cbf4`  
		Last Modified: Tue, 02 Jul 2024 04:33:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92e17a5667c973237880379e1fc188c1530f8dedf2dfadf57f47e2f73108901`  
		Last Modified: Tue, 02 Jul 2024 04:33:24 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094f8020d23ab0c65a3ffea4a1e522fd154a3ec820bd1e71daac119949ccd2e5`  
		Last Modified: Wed, 03 Jul 2024 10:27:33 GMT  
		Size: 22.1 MB (22067289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa36ab13a90403a6cf9e2d309f8bdfae41b9edd622140503f232187be03b7252`  
		Last Modified: Wed, 03 Jul 2024 10:27:33 GMT  
		Size: 9.2 MB (9161594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b741333052f1314cd99b62ad5d9290c1b6b92f42e98690a051893a7881c494b8`  
		Last Modified: Wed, 03 Jul 2024 10:27:32 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f977a6f39040974c36ebf53562479d4b68ce2c29d930cea0f632e1105fe7f7`  
		Last Modified: Wed, 03 Jul 2024 10:27:32 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229ec741b036dac82a7a35cf0e4154a9d92ece844748535d5c281cc4364a4da`  
		Last Modified: Wed, 03 Jul 2024 10:27:33 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11` - unknown; unknown

```console
$ docker pull maven@sha256:5e0e7a9e2fa0d81f2bb07de55d14ee50ac7121a27caa8bd77eec0deb5311fd72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4897224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18fd5a5f9cad3e1a37847f9015e13bbdd87241df67d0be47aff8cd88b3300636`

```dockerfile
```

-	Layers:
	-	`sha256:8bb7097e99d1d492a6a51c2e8c34224e74fc8cddb7add497d6df23c5c9071908`  
		Last Modified: Wed, 03 Jul 2024 10:27:32 GMT  
		Size: 4.9 MB (4872715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd5928b8b07477ecb926e8e0808f8dec9de1946770b3e4440d681323d0e028fc`  
		Last Modified: Wed, 03 Jul 2024 10:27:32 GMT  
		Size: 24.5 KB (24509 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:41a801601dc0db43fe4f1e5d6e4259cec24f9b3d760d117fbab8264d32b6f4ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.5 MB (211457343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0caa562db2fd1dac2ffa15ab1f74a991127ae187e97b786570e462cdb64e0b`
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
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8389baa7e66b9c7baef599308d6321afd34400b3830044b864bc82e8b7f41bc0`  
		Last Modified: Tue, 02 Jul 2024 04:34:23 GMT  
		Size: 12.8 MB (12812967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4581c0454f33f7cb90c1ac162639bca362cb8a7f40732b2f81407f0354c26085`  
		Last Modified: Tue, 02 Jul 2024 04:35:02 GMT  
		Size: 142.3 MB (142311039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccca8a43f3b770e08c6d90548988f806796221cdd0d51ab0c360dab46d38fc6`  
		Last Modified: Tue, 02 Jul 2024 04:34:52 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:051f223486bb03134f3fcf7de029b06e9ce5dca21838063eed2e8a5d823da8d0`  
		Last Modified: Tue, 02 Jul 2024 04:34:01 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c4d0f5a597bbc6f27e9cc77fd63ec6891930ea7f08f54ccbcda694ae6338a9`  
		Last Modified: Wed, 03 Jul 2024 01:39:25 GMT  
		Size: 18.8 MB (18768373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69da140aa912837c472358b64ca234213d513e2b2bd898c3581d6936766517ff`  
		Last Modified: Wed, 03 Jul 2024 01:39:25 GMT  
		Size: 9.2 MB (9161564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b72da44bafa92038d92b6103daf7ae9e3184bc4cb43b2fb9c2775a09fc4cef1f`  
		Last Modified: Wed, 03 Jul 2024 01:39:24 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5c53d7026b4269a98a60f2b284d33db8d5c1377ca8e809d829004d67d2450d`  
		Last Modified: Wed, 03 Jul 2024 01:39:24 GMT  
		Size: 358.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fa4ab60231f1ec92664dbc2f345f91d113180e35ffe9554dc72d61cbd0ea70`  
		Last Modified: Wed, 03 Jul 2024 01:39:25 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11` - unknown; unknown

```console
$ docker pull maven@sha256:3cd8c35373059ef39bce782952cece7ff0e20c4b79cb9a4bc4dfbdd632825b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4903653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13dd823f8e9745e14307a4b7b36f1c14db2a207860cf9970dc24d64c39d3f4f2`

```dockerfile
```

-	Layers:
	-	`sha256:3c187f3ec36b28b96331a10129ac0dfc3248662743b3002a776118fb7b2fd62f`  
		Last Modified: Wed, 03 Jul 2024 01:39:24 GMT  
		Size: 4.9 MB (4878973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1367a56aa18d9b1d34a6a0d95750280060f3bc1463f6cb4729fe03d9c6b761e`  
		Last Modified: Wed, 03 Jul 2024 01:39:24 GMT  
		Size: 24.7 KB (24680 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-11` - linux; ppc64le

```console
$ docker pull maven@sha256:00dc5f45d62642b6c43c75999b55a7d3f608fdd59aa393f5dc055f090b33b86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **213.0 MB (213043146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95910a6d45791b87e5cb099b5d56c96fe2fdda90bef0226d9eb17402ec3668e`
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
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:e2e1e840070a30a93a9141ddf77b416d95fb822ac1f550f7162a64e18e0ade5b in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:8abbcd57d9001f5aade9e7c1c7cf47fea659efa1b67f1bf51c65e0f66569df0d`  
		Last Modified: Tue, 02 Jul 2024 02:09:14 GMT  
		Size: 35.6 MB (35588321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aea30364eff82eb5379f35c10575a54ece802a6af1763591c0a6a999d72c84c`  
		Last Modified: Tue, 02 Jul 2024 05:04:14 GMT  
		Size: 13.7 MB (13714876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e3c3db8c3ce267302ab33698998e2969d08346da85f3c69446c98910f01e534`  
		Last Modified: Tue, 02 Jul 2024 05:04:57 GMT  
		Size: 132.7 MB (132718876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2731f957d26e7380c16b0db866ae857ccea882ea104b9cadde90f6da05365bc`  
		Last Modified: Tue, 02 Jul 2024 05:04:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34895e55ab2f8114aef706c3814ecaad2fb5146d3efb7b13533c5383c9527eb3`  
		Last Modified: Tue, 02 Jul 2024 05:04:45 GMT  
		Size: 733.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ae226c2ff23972ce3c9f055d6d9dc9c73301cea428ccd817f894bfc5609f12`  
		Last Modified: Wed, 03 Jul 2024 08:15:19 GMT  
		Size: 21.9 MB (21857224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99e9068edfb39a94dbb00611c135966634b52d137df86d710ea26d5e5ed712d`  
		Last Modified: Wed, 03 Jul 2024 08:15:19 GMT  
		Size: 9.2 MB (9161579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294264be876a471c9f8d80d459f30d512e359b284df5f512af1f20067bf4fa3f`  
		Last Modified: Wed, 03 Jul 2024 08:15:18 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdfd49c3c1667cdceb1cc35e7615600ee2f48acb543cf32f2532f41d923dae4`  
		Last Modified: Wed, 03 Jul 2024 08:15:18 GMT  
		Size: 359.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8949fbdfaf55aa3564a9b0a745bc57e7bb4997371a729bb368f8adb483f7f25a`  
		Last Modified: Wed, 03 Jul 2024 08:15:20 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11` - unknown; unknown

```console
$ docker pull maven@sha256:1fe402e8dbcc0f3e347cfe7679a43347d69759867ad852631e1365ae7d406a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4904274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3411936ae0f54cc5678ea1f161a84e1955e47e174bbb9cff7a1689ae9328907e`

```dockerfile
```

-	Layers:
	-	`sha256:6b0641ebef00f494ff40f154c87c1185468670ff14a36e6d2228cce5e0dabb62`  
		Last Modified: Wed, 03 Jul 2024 08:15:19 GMT  
		Size: 4.9 MB (4879851 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1afd076e717f281bd879cf60b4c8eb6c53eb87882768105a6c082296fb83be09`  
		Last Modified: Wed, 03 Jul 2024 08:15:18 GMT  
		Size: 24.4 KB (24423 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-eclipse-temurin-11` - linux; s390x

```console
$ docker pull maven@sha256:0ec81a8810cd20615ef771f2f7f11e9ebb7700dfb5207f694504ff03a9abbd24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.2 MB (195243485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9751377922761e184f6ef5ccaf1958aec733d7f31f3dba2624e9f2752ac7a48`
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
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 09:17:07 GMT
ADD file:160bc105c5c70c3239daf08894bd8a2311ea04a965b30820eebf28573143f86b in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 23 Apr 2024 20:51:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 Apr 2024 20:51:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENV JAVA_VERSION=jdk-11.0.23+9
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e00476a7be3c4adfa9b3d55d30768967fd246a8352e518894e183fa444d4d3ce';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.23_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='23e47ea7a3015be3240f21185fd902adebdcf76530757c9b482c7eb5bd3417c2';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_x64_linux_hotspot_11.0.23_9.tar.gz';          ;;        armhf|arm)          ESUM='8077edc07a57d846c3d11286a7caf05ed6ca6d6c1234bf0e03611f18e187f075';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_arm_linux_hotspot_11.0.23_9.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='f56068bb64c6bf858894f75c2bc261f54db32932422eb07527f36ae40046e9a0';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.23_9.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='cf06c3e41acfaeda77112ac04f5a711cafe9fa9ac04dff758696fe7e8d66a0ea';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.23%2B9/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.23_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
COPY entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 23 Apr 2024 20:51:38 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 23 Apr 2024 20:51:38 GMT
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
COPY mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY settings-docker.xml /usr/share/maven/ref/ # buildkit
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
	-	`sha256:4870604a2dd3e1b2f1a9f9dc1f8d02b548d030f0680887506b32aaee40747aa4`  
		Last Modified: Tue, 02 Jul 2024 03:47:54 GMT  
		Size: 28.6 MB (28637470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eaa70dc31cdad42121b062dd92b14960ba0a992a5bedede9795f6d11bf4a38`  
		Last Modified: Tue, 02 Jul 2024 03:54:48 GMT  
		Size: 13.0 MB (12954922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc962421b172d90113303487a4015173172ddf2dfcb92594f21552cbdcdf113`  
		Last Modified: Tue, 02 Jul 2024 03:54:56 GMT  
		Size: 125.5 MB (125501659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93a8fc8c06bd2fe8351f71897ec35f2a9263a79cba63ae843f55c34f08ca640`  
		Last Modified: Tue, 02 Jul 2024 03:54:47 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:364fc43aba6ceeb1055e0ddb36f97ca8e60d271a307dbd34342dca6bd24fbed1`  
		Last Modified: Tue, 02 Jul 2024 03:54:47 GMT  
		Size: 734.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f51b9927f86ef67aa57fcc6773dcea13e38660b536e2393b34dfbbf6401cb6c`  
		Last Modified: Wed, 03 Jul 2024 01:05:33 GMT  
		Size: 19.0 MB (18985560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08b46f2067a2441a4cf98c2939f2aba890e0170c4f5aa3ac38ef268a54e21ad`  
		Last Modified: Wed, 03 Jul 2024 01:05:34 GMT  
		Size: 9.2 MB (9161598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe9ea556b573858cc33b8d0f67f7a51b051fcf2f0b84eef464a446011269e14`  
		Last Modified: Wed, 03 Jul 2024 01:05:33 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cef34b22e1b08afa271ddde0f28b87c11c60c756491d9043f914401533ea711c`  
		Last Modified: Wed, 03 Jul 2024 01:05:33 GMT  
		Size: 363.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbec54152625c6dfd1662ab46476321ce63cde566bc9d2677412736a31c38d2`  
		Last Modified: Wed, 03 Jul 2024 01:05:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11` - unknown; unknown

```console
$ docker pull maven@sha256:9dec736b7e5cb42c98a28bbb807e8e3d9baf42d1676151c40a357810e30bcd28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4897087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c54329ffb867268f1d25705df8d70c77a476ca745f688569ebfcd9992698ab8`

```dockerfile
```

-	Layers:
	-	`sha256:0b17392594315ce60e25b71482346e985befb90e580f17baae4bbdaa8da97fdc`  
		Last Modified: Wed, 03 Jul 2024 01:05:33 GMT  
		Size: 4.9 MB (4872705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e63c2d65204772c9b693a75e82dcb789087d5be45386ba20ea217ab34061728`  
		Last Modified: Wed, 03 Jul 2024 01:05:33 GMT  
		Size: 24.4 KB (24382 bytes)  
		MIME: application/vnd.in-toto+json
