## `xwiki:mariadb-tomcat`

```console
$ docker pull xwiki@sha256:eb6ddcc53abe6dfab8f9ab26819e4d9fe119867c61605c7716c7786b7301aef0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `xwiki:mariadb-tomcat` - linux; amd64

```console
$ docker pull xwiki@sha256:195709c768c90adc6ee844d42e64c9e2946c0f2d0f7f75855024d837fea56f54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **626.1 MB (626091720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b13bf7164691e0848e5cb41f5fce0e500208895fbf2d3c0c5a61284dbcc7b6c9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 28 Jul 2025 13:28:25 GMT
ARG RELEASE
# Mon, 28 Jul 2025 13:28:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Jul 2025 13:28:25 GMT
ADD file:98599296b3845cfad0ddc91f054e32ed9bcdefd76dd7b6dcf64fa3e2d648d018 in / 
# Mon, 28 Jul 2025 13:28:25 GMT
CMD ["/bin/bash"]
# Mon, 28 Jul 2025 13:28:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Jul 2025 13:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Jul 2025 13:28:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Jul 2025 13:28:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 28 Jul 2025 13:28:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Jul 2025 13:28:25 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
WORKDIR /usr/local/tomcat
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 28 Jul 2025 13:28:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_MAJOR=10
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_VERSION=10.1.44
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Mon, 28 Jul 2025 13:28:25 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Jul 2025 13:28:25 GMT
ENTRYPOINT []
# Mon, 28 Jul 2025 13:28:25 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Jul 2025 13:28:25 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENV XWIKI_VERSION=17.6.0
# Mon, 28 Jul 2025 13:28:25 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.6.0
# Mon, 28 Jul 2025 13:28:25 GMT
ENV XWIKI_DOWNLOAD_SHA256=3a5f30089da81f41e861a90814c82e819daad5fc63d1d112573dd3671e9f3d47
# Mon, 28 Jul 2025 13:28:25 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_VERSION=3.5.4
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_SHA256=9cac1a01e3b2bac18f826d48475b93e6bdb5c16d31f7227f9653c7c8f1b378e7
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.4
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.4.jar
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.4.jar
# Mon, 28 Jul 2025 13:28:25 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Jul 2025 13:28:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Jul 2025 13:28:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:b71466b94f266b4c2e0881749670e5b88ab7a0fd4ca4a4cdf26cb45e4bde7e4e`  
		Last Modified: Wed, 30 Jul 2025 10:35:12 GMT  
		Size: 29.7 MB (29723215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c1ceb63b80a861ae319235f3b1e3e392279a30c5cc9f0dec5c5582505b55f8`  
		Last Modified: Tue, 12 Aug 2025 17:24:47 GMT  
		Size: 17.0 MB (16971683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f62b74addfec2b46a83d8e9d131c7c6563aa4399f142b91d977d506f6c137dcb`  
		Last Modified: Tue, 12 Aug 2025 17:25:01 GMT  
		Size: 53.0 MB (52968913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ac95b0cea99b9ed5ddc084d329fc5e139c2adde65e599e4f9803bd9aa474ef`  
		Last Modified: Tue, 12 Aug 2025 17:24:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cce32af8d45a5194c78928090c5748f048a001dcd13b737c7a2992892753871`  
		Last Modified: Tue, 12 Aug 2025 17:24:49 GMT  
		Size: 2.3 KB (2282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26601cb9a1d4d844a296eb3e1788428e0f0ed793b7b7d2c299692fedf35d5740`  
		Last Modified: Tue, 12 Aug 2025 18:08:43 GMT  
		Size: 138.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858c4b60ed3f0a36f7205bdeca07b3161e5ba5259b116fa63b99c1ae8d741852`  
		Last Modified: Tue, 12 Aug 2025 18:08:45 GMT  
		Size: 14.1 MB (14081081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:657236842a194fb380adac21a58c1578dcbac33ce697252d79d5fe9d464ce534`  
		Last Modified: Tue, 12 Aug 2025 18:08:45 GMT  
		Size: 224.7 KB (224702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c1e4d3c7661d39c68aef2cf48c688d1e21123366f536f0b98ffaff6a3b8cdf`  
		Last Modified: Tue, 12 Aug 2025 21:27:53 GMT  
		Size: 191.2 MB (191178557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deaec35d29edcb5933bf84b7dd790fcd4749a44373b37c06792e43701827009`  
		Last Modified: Tue, 12 Aug 2025 21:28:01 GMT  
		Size: 320.2 MB (320233314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5527aaffe0ea5b9810c41a1b18b155f623fda8655637b3fe7b3f51a61c6848bc`  
		Last Modified: Tue, 12 Aug 2025 19:04:00 GMT  
		Size: 695.0 KB (694958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3e2031a467e1f1294539e5d32b76b750c4ccad46dce04f25923d7566e19021`  
		Last Modified: Tue, 12 Aug 2025 19:04:03 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b77839efb5d21673c7c48aecac12106770d0ffe4954091f96ed0f68b53842e34`  
		Last Modified: Tue, 12 Aug 2025 19:04:01 GMT  
		Size: 2.3 KB (2306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6674fe1a4741208254412167c227cc44c004aeff4da099d73e80858889e8bda`  
		Last Modified: Tue, 12 Aug 2025 19:04:02 GMT  
		Size: 6.5 KB (6534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3a328ce680b796484f78879dec95760a10a724463d864c3765e65bbb046407d`  
		Last Modified: Tue, 12 Aug 2025 19:04:01 GMT  
		Size: 2.5 KB (2472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:287bb5476700e7b5b33bad4da6f5c1e65e144a997a6b77dee3184ab3655635e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9193717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8b59de5d8f114423e051157d0c85f9fbb36662ac57f0fa056e056f8b7dc91e`

```dockerfile
```

-	Layers:
	-	`sha256:452c62d12755976ea36022e889ce89e3df71025aa3f76e87b622b13972d1f159`  
		Last Modified: Tue, 12 Aug 2025 21:07:51 GMT  
		Size: 9.2 MB (9152916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21a6a6baff58d95cbf84d103f017197ba392cdbc0d6bac90c4154d9732d6b7d1`  
		Last Modified: Tue, 12 Aug 2025 21:07:52 GMT  
		Size: 40.8 KB (40801 bytes)  
		MIME: application/vnd.in-toto+json

### `xwiki:mariadb-tomcat` - linux; arm64 variant v8

```console
$ docker pull xwiki@sha256:8fb9a198cbc2553fb3a5ec158f2d9ddebbbc7dee77cce4cc9264f44cbbb4366e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **622.1 MB (622088458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c947de9ae432ec56bb442011c91c1327e5b1a349fb239438cedf76242541d2ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["xwiki"]`

```dockerfile
# Mon, 28 Jul 2025 13:28:25 GMT
ARG RELEASE
# Mon, 28 Jul 2025 13:28:25 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 28 Jul 2025 13:28:25 GMT
ADD file:e189629238f69759e9c6cb1cac039ece646eeecb640e5eb670e5cf92543b46fb in / 
# Mon, 28 Jul 2025 13:28:25 GMT
CMD ["/bin/bash"]
# Mon, 28 Jul 2025 13:28:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 28 Jul 2025 13:28:25 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Jul 2025 13:28:25 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         gnupg         fontconfig         ca-certificates p11-kit         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        amd64)          ESUM='968c283e104059dae86ea1d670672a80170f27a39529d815843ec9c1f0fa2a03';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_linux_hotspot_21.0.8_9.tar.gz';          ;;        arm64)          ESUM='f54f6e2a907c4aef95ce6d7388474c6d5d87ae87899dd309561672bcfda9121e';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_aarch64_linux_hotspot_21.0.8_9.tar.gz';          ;;        ppc64el)          ESUM='12c351c7a6906ca4ddd3f158cbd9ebf2733bab2dc432dc3f9d5685476b16b7bc';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_ppc64le_linux_hotspot_21.0.8_9.tar.gz';          ;;        riscv64)          ESUM='1c87410971cd7c3cd175bfe81cfecbe83462a64291caf1055cdcc0feb56e907d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_riscv64_linux_hotspot_21.0.8_9.tar.gz';          ;;        s390x)          ESUM='7f2f9e48cc0e970b671b4ee8c69bf98002e27e4546e0c33071a2ecac38a8154c';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_s390x_linux_hotspot_21.0.8_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     wget --progress=dot:giga -O /tmp/openjdk.tar.gz.sig ${BINARY_URL}.sig;     export GNUPGHOME="$(mktemp -d)";     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 3B04D753C9050D9A5D343F39843C48A565F8F04B;     gpg --batch --verify /tmp/openjdk.tar.gz.sig /tmp/openjdk.tar.gz;     rm -rf "${GNUPGHOME}" /tmp/openjdk.tar.gz.sig;     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump; # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux;     echo "Verifying install ...";     echo "java --version"; java --version;     echo "Complete." # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 28 Jul 2025 13:28:25 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Mon, 28 Jul 2025 13:28:25 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Jul 2025 13:28:25 GMT
RUN mkdir -p "$CATALINA_HOME" # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
WORKDIR /usr/local/tomcat
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Mon, 28 Jul 2025 13:28:25 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_MAJOR=10
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_VERSION=10.1.44
# Mon, 28 Jul 2025 13:28:25 GMT
ENV TOMCAT_SHA512=efc5f010d2c35c7f930b8d53e809eb72ac95675e739c9678e617f42c704ebe6410676071b1118c429cc84eb651e50241fd8fe4bf21be8f3a12d00e9fb28e1610
# Mon, 28 Jul 2025 13:28:25 GMT
COPY /usr/local/tomcat /usr/local/tomcat # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 28 Jul 2025 13:28:25 GMT
ENTRYPOINT []
# Mon, 28 Jul 2025 13:28:25 GMT
CMD ["catalina.sh" "run"]
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.authors=XWiki Development Team <committers@xwiki.org>
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.url=https://hub.docker.com/_/xwiki
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.documentation=https://hub.docker.com/_/xwiki
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.source=https://github.com/xwiki/xwiki-docker.git
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.vendor=xwiki.org
# Mon, 28 Jul 2025 13:28:25 GMT
LABEL org.opencontainers.image.licenses=LGPL-2.1
# Mon, 28 Jul 2025 13:28:25 GMT
RUN apt-get update &&   apt-get --no-install-recommends -y install     curl     libreoffice     unzip     procps &&   rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENV XWIKI_VERSION=17.6.0
# Mon, 28 Jul 2025 13:28:25 GMT
ENV XWIKI_URL_PREFIX=https://maven.xwiki.org/releases/org/xwiki/platform/xwiki-platform-distribution-war/17.6.0
# Mon, 28 Jul 2025 13:28:25 GMT
ENV XWIKI_DOWNLOAD_SHA256=3a5f30089da81f41e861a90814c82e819daad5fc63d1d112573dd3671e9f3d47
# Mon, 28 Jul 2025 13:28:25 GMT
RUN rm -rf /usr/local/tomcat/webapps/* &&   mkdir -p /usr/local/tomcat/temp &&   mkdir -p /usr/local/xwiki/data &&   curl -fSL "${XWIKI_URL_PREFIX}/xwiki-platform-distribution-war-${XWIKI_VERSION}.war" -o xwiki.war &&   echo "$XWIKI_DOWNLOAD_SHA256 xwiki.war" | sha256sum -c - &&   unzip -d /usr/local/tomcat/webapps/ROOT xwiki.war &&   rm -f xwiki.war # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_VERSION=3.5.4
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_SHA256=9cac1a01e3b2bac18f826d48475b93e6bdb5c16d31f7227f9653c7c8f1b378e7
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_PREFIX=https://repo1.maven.org/maven2/org/mariadb/jdbc/mariadb-java-client/3.5.4
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_ARTIFACT=mariadb-java-client-3.5.4.jar
# Mon, 28 Jul 2025 13:28:25 GMT
ENV MARIADB_JDBC_TARGET=/usr/local/tomcat/webapps/ROOT/WEB-INF/lib/mariadb-java-client-3.5.4.jar
# Mon, 28 Jul 2025 13:28:25 GMT
RUN curl -fSL "${MARIADB_JDBC_PREFIX}/${MARIADB_JDBC_ARTIFACT}" -o $MARIADB_JDBC_TARGET &&   echo "$MARIADB_JDBC_SHA256 $MARIADB_JDBC_TARGET" | sha256sum -c - # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY tomcat/setenv.sh /usr/local/tomcat/bin/ # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY xwiki/hibernate.cfg.xml /usr/local/tomcat/webapps/ROOT/WEB-INF/hibernate.cfg.xml # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
RUN sed -i 's/<id>org.xwiki.platform:xwiki-platform-distribution-war/<id>org.xwiki.platform:xwiki-platform-distribution-docker/'   /usr/local/tomcat/webapps/ROOT/META-INF/extension.xed # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
COPY xwiki/docker-entrypoint.sh /usr/local/bin/docker-entrypoint.sh # buildkit
# Mon, 28 Jul 2025 13:28:25 GMT
VOLUME [/usr/local/xwiki]
# Mon, 28 Jul 2025 13:28:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 28 Jul 2025 13:28:25 GMT
CMD ["xwiki"]
```

-	Layers:
	-	`sha256:49a8ca9a328e179fe07d40f7f2fd5fb2860b5c45463c288b64f05be521173d2e`  
		Last Modified: Wed, 30 Jul 2025 10:35:20 GMT  
		Size: 28.9 MB (28860377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3eefddfbcab06ca4f10ce56a232d4ec2d822b72ac91b8958abc9acd3c4223c`  
		Last Modified: Tue, 12 Aug 2025 18:31:54 GMT  
		Size: 17.0 MB (16988833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2683f57ecc3239b77668933adbcb066b796b3d8385694028dfa534473428efe9`  
		Last Modified: Tue, 12 Aug 2025 18:39:53 GMT  
		Size: 52.1 MB (52148453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1835951682aea5916d97b15850e70d45156732945ac0dbb2535d8c6306228f`  
		Last Modified: Tue, 12 Aug 2025 18:39:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766ee17d70f62cab7ff1f4f47b0567a37c24335c88c58b652cb5b22e4f7e92e0`  
		Last Modified: Tue, 12 Aug 2025 18:39:43 GMT  
		Size: 2.3 KB (2283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d8672b50cb4a092687fe9a28d3978851b924618ac39a15dae4dadfaadaf822e`  
		Last Modified: Wed, 13 Aug 2025 14:31:22 GMT  
		Size: 139.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e52672eb39ed2019c53a3f3603ad519204a0c29fde83143a5a10d3bfa573fe`  
		Last Modified: Wed, 13 Aug 2025 14:31:28 GMT  
		Size: 14.1 MB (14083963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f0c184de15ddea7dc3c1d0573a452b3adbbf330734ecbd820eba457e4c5f7e`  
		Last Modified: Wed, 13 Aug 2025 14:31:22 GMT  
		Size: 225.1 KB (225130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6078cc14a57aeefbb3f0f83c3d945b628b01bbef247cd5904fa8d79f12ad957c`  
		Last Modified: Wed, 13 Aug 2025 20:20:59 GMT  
		Size: 188.8 MB (188838125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc2a62281b4a83f8bea34d6129f4014ec8b8f4d224e739e7e30ec7fe03db7d0`  
		Last Modified: Wed, 13 Aug 2025 20:21:14 GMT  
		Size: 320.2 MB (320233313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9264d82ee11922cd0c979af20b7a09b359a46be4ed7122d48051820e34f2d4f8`  
		Last Modified: Wed, 13 Aug 2025 19:07:08 GMT  
		Size: 695.0 KB (694959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a08f6dff8f7ebdfbec316447f0ca5cc7a0bf56e935ca762a22fdaa28fd0f12`  
		Last Modified: Wed, 13 Aug 2025 19:07:09 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db79e1ecf08aa4ba50eeaaa594f2e9588aa6896a5c690683e999c3be1a223504`  
		Last Modified: Wed, 13 Aug 2025 19:19:17 GMT  
		Size: 2.3 KB (2310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9383f452b92705ebf994304623d9dc1228a42b255c41ed06aa539aebd28bf57e`  
		Last Modified: Wed, 13 Aug 2025 19:19:20 GMT  
		Size: 6.5 KB (6537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84939a106d2cd548a16b06c0ac3cb29dc0dfa8c863647dac8d5d9d903fe87708`  
		Last Modified: Wed, 13 Aug 2025 19:19:24 GMT  
		Size: 2.5 KB (2473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `xwiki:mariadb-tomcat` - unknown; unknown

```console
$ docker pull xwiki@sha256:d2baeff5004933b1fee5d87c473f21dfdb0b97c7046b042d5930869701fb2638
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.2 MB (9194643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43809b2532e0791e1f278a447f572b9ca1e69934b08eee2193d88947e82ca3ea`

```dockerfile
```

-	Layers:
	-	`sha256:756adf2df5eace4102f50647bad77f03c47c0745b0b4ec61732eaaef61433695`  
		Last Modified: Wed, 13 Aug 2025 21:08:17 GMT  
		Size: 9.2 MB (9153669 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:282e313007b5f2ed43440ac8d701625a0d1f28d82a61727293eec0c4e6cf73ac`  
		Last Modified: Wed, 13 Aug 2025 21:08:18 GMT  
		Size: 41.0 KB (40974 bytes)  
		MIME: application/vnd.in-toto+json
