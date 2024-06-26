## `ibm-semeru-runtimes:open-21.0.3_9-jre`

```console
$ docker pull ibm-semeru-runtimes@sha256:0793a219a674b64d0dee4216dc9be10e54477f1cc0ba810e4e0403a1e22dddc1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `ibm-semeru-runtimes:open-21.0.3_9-jre` - linux; amd64

```console
$ docker pull ibm-semeru-runtimes@sha256:3da63360daff1d25455d04c1af00e73c228237f736622a3fe549fe111ef28a74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103107084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2930c9520fe8d285d5960f241c6931f6124c3c478ce7476c79d1176c9439466a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:32:23 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:32:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:32:23 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:32:25 GMT
ADD file:89847d76d242dea90ede05e9e1e13a1ff4400a65eafbe2d6e31e086c93893580 in / 
# Mon, 03 Jun 2024 10:32:26 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-21.0.3+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0222dc3749e1c94bd1b047cdb02eb18310aefd9f7965b66196da06e4e3844b7a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b831e8c418374ccec13c51f60c36f4c32266f3cc83cb31f32286f89c26d66e00';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a2058c477df602e34d13bcdd45811abe592c72765e7f0c48c72771df22ef406b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='9c9fcc534723f8a454e4f788b1ea703bdaa91db3eaa2f9167d53123483ec66d0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:7646c8da332499ae416b15479ce832db32e39a501c662e24324f595509a0d3db`  
		Last Modified: Mon, 03 Jun 2024 10:46:44 GMT  
		Size: 29.5 MB (29533754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:668af547d451b6d9250fef09f1e229df2713e86e628d3acb16c2c7c5cd922926`  
		Last Modified: Tue, 25 Jun 2024 22:57:45 GMT  
		Size: 12.2 MB (12156381 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340a947e10e5cb0ad4abf12f9b28b4bdd7f13ea00c134cc62194aa01bb64d43b`  
		Last Modified: Tue, 25 Jun 2024 22:57:46 GMT  
		Size: 56.3 MB (56344536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b53612068546394d43051bac679281820a21b205f6e1ee7126cb4706a3f1eb2`  
		Last Modified: Tue, 25 Jun 2024 22:57:45 GMT  
		Size: 5.1 MB (5072413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.3_9-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:a0d62f423ea6256b6159884b1023299135b01788a1cd09fe900b9df34f800b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f89a7f156bde7ef97f22b5ab5b4e8bf41fe5804496c82ec4c3cc614d1ca6438f`

```dockerfile
```

-	Layers:
	-	`sha256:376be8eee689501501d13fef90590c47c8e02f3fcb7e702b3c848415bd56fa0b`  
		Last Modified: Tue, 25 Jun 2024 22:57:45 GMT  
		Size: 3.4 MB (3433987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79adb40edda5f150e602541dfbf3a867099b7f4fb0e123b48c53624b885a682c`  
		Last Modified: Tue, 25 Jun 2024 22:57:45 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.3_9-jre` - linux; arm64 variant v8

```console
$ docker pull ibm-semeru-runtimes@sha256:044b953bd2cf337f1ffec1d809d9709968a9e3a2cffb6ea80d2243f407e69f37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.7 MB (96663883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71d90672b1aa5dbb23e47de04a8ffd7ae22b5e448f96adcd6d333a2f1f744569`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:30:07 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:30:07 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:30:07 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:30:11 GMT
ADD file:5f73ea0f53302f1771b6d2cb5650f715247ad02d80e986d67b2d55c22712f1ca in / 
# Mon, 03 Jun 2024 10:30:12 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-21.0.3+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0222dc3749e1c94bd1b047cdb02eb18310aefd9f7965b66196da06e4e3844b7a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b831e8c418374ccec13c51f60c36f4c32266f3cc83cb31f32286f89c26d66e00';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a2058c477df602e34d13bcdd45811abe592c72765e7f0c48c72771df22ef406b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='9c9fcc534723f8a454e4f788b1ea703bdaa91db3eaa2f9167d53123483ec66d0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:9b10a938e28486049341cb41134e8c0c141b2e25870896c597e2a54df471acbb`  
		Last Modified: Mon, 03 Jun 2024 10:46:52 GMT  
		Size: 27.4 MB (27361782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48ee6e790fe3be315f574c78a35fef5e2104480be37cd385884a99abf457a751`  
		Last Modified: Tue, 25 Jun 2024 23:02:58 GMT  
		Size: 12.1 MB (12115683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bcf9b4d861dcff568be879d8b73d2bced38ea2d89a0354b0fdd6d0ddfa747af`  
		Last Modified: Tue, 25 Jun 2024 23:29:55 GMT  
		Size: 52.4 MB (52352070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6c4a9919ccfa97a0c54208ac80ce6d0227dfe382eecd242bc1f345d1cf4b08`  
		Last Modified: Tue, 25 Jun 2024 23:29:53 GMT  
		Size: 4.8 MB (4834348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.3_9-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:865732fc3b4c8950ed77739802b3360558843ef15b59a4ff33516ae1b06bd156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3458975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9b5ae693edc4608756d9e7273a1af2273c620e4e15111e83b27b747c3ecf0d0`

```dockerfile
```

-	Layers:
	-	`sha256:ac9a8564ab7bc01110e073a20f64107f2838504a0d88fb9a57320a078e607733`  
		Last Modified: Tue, 25 Jun 2024 23:29:53 GMT  
		Size: 3.4 MB (3434276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e787f8bfa41e2710ddc2c6d335c8f37813aab8fc737235734fe280269e9e9caf`  
		Last Modified: Tue, 25 Jun 2024 23:29:53 GMT  
		Size: 24.7 KB (24699 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.3_9-jre` - linux; ppc64le

```console
$ docker pull ibm-semeru-runtimes@sha256:b70173303ec35c7c83ff608afb9e18b54e22ac5c1cd7826c2e360d0e4d5e3c0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **108.9 MB (108943015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14d1e900216b2251f380d7c8c40e5c4559ae76727a0b33fad29578c6198e3d7e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:34:18 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:34:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:34:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:34:22 GMT
ADD file:a220ef67c41f76acc5934568443ce6faeaeba3de0ab529ab7b3b3172122c9adb in / 
# Mon, 03 Jun 2024 10:34:22 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-21.0.3+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0222dc3749e1c94bd1b047cdb02eb18310aefd9f7965b66196da06e4e3844b7a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b831e8c418374ccec13c51f60c36f4c32266f3cc83cb31f32286f89c26d66e00';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a2058c477df602e34d13bcdd45811abe592c72765e7f0c48c72771df22ef406b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='9c9fcc534723f8a454e4f788b1ea703bdaa91db3eaa2f9167d53123483ec66d0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:53046b5e4efb6dbf3a776302592f40c8d0ac09b5738be07d28c7f3be6b7e1e08`  
		Last Modified: Mon, 03 Jun 2024 10:47:05 GMT  
		Size: 34.5 MB (34460693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c866879b3eaab6a2be320ab73cc032a3c43ef798a2582028559e9055cc257b5`  
		Last Modified: Tue, 25 Jun 2024 23:04:25 GMT  
		Size: 12.9 MB (12887989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35a965f91107a8342426c0ade52100b838086bba634281df17e4d7daccf49c14`  
		Last Modified: Tue, 25 Jun 2024 23:38:23 GMT  
		Size: 57.7 MB (57672386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3339347927ecf03e23e0741ba8ee6d23ce879d9b695f937e3517abad3f1d6b`  
		Last Modified: Tue, 25 Jun 2024 23:38:22 GMT  
		Size: 3.9 MB (3921947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.3_9-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ede9d60981263c6fdad341dc2af3e67ed152b4a537b2c7b684c14a3e26b05851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3462927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e24654dfb3dcec102963e1332b8bb3e35f8463f674d15376aea7a053d1637f`

```dockerfile
```

-	Layers:
	-	`sha256:424399831967de4eac05d43eb9f376f8d59fc679b00d4605cd2f2cee805c8b92`  
		Last Modified: Tue, 25 Jun 2024 23:38:22 GMT  
		Size: 3.4 MB (3438487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a067c30c13be66c1a3a05e19ee0f56769a5bd5da4502101dd32b49b430122291`  
		Last Modified: Tue, 25 Jun 2024 23:38:21 GMT  
		Size: 24.4 KB (24440 bytes)  
		MIME: application/vnd.in-toto+json

### `ibm-semeru-runtimes:open-21.0.3_9-jre` - linux; s390x

```console
$ docker pull ibm-semeru-runtimes@sha256:b190084498200dce6244bb3ddb2cae13e4b22f32866ca96f65d3e65b989e957c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.4 MB (100376438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88f941fcf749f4004de6c0767c656856d6168e196c5cc72de8050ae7ab44ae64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Jun 2024 10:29:44 GMT
ARG RELEASE
# Mon, 03 Jun 2024 10:29:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Jun 2024 10:29:44 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 03 Jun 2024 10:29:47 GMT
ADD file:4fb908f3bd908a7abc338d7e2006cb2c97aa7f83aca415f3b86c0ae86d61fed1 in / 
# Mon, 03 Jun 2024 10:29:47 GMT
CMD ["/bin/bash"]
# Tue, 04 Jun 2024 05:42:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 04 Jun 2024 05:42:02 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_VERSION=jdk-21.0.3+9_openj9-0.44.0
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='0222dc3749e1c94bd1b047cdb02eb18310aefd9f7965b66196da06e4e3844b7a';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_aarch64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        amd64|x86_64)          ESUM='b831e8c418374ccec13c51f60c36f4c32266f3cc83cb31f32286f89c26d66e00';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_x64_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='a2058c477df602e34d13bcdd45811abe592c72765e7f0c48c72771df22ef406b';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_ppc64le_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        s390x)          ESUM='9c9fcc534723f8a454e4f788b1ea703bdaa91db3eaa2f9167d53123483ec66d0';          BINARY_URL='https://github.com/ibmruntimes/semeru21-binaries/releases/download/jdk-21.0.3%2B9_openj9-0.44.0/ibm-semeru-open-jre_s390x_linux_21.0.3_9_openj9-0.44.0.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz; # buildkit
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Jun 2024 05:42:02 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+PortableSharedCache -XX:+IdleTuningGcOnIdle -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,readonly,nonFatal
# Tue, 04 Jun 2024 05:42:02 GMT
RUN set -eux;     unset OPENJ9_JAVA_OPTIONS;     SCC_SIZE="50m";     DOWNLOAD_PATH_TOMCAT=/tmp/tomcat;     INSTALL_PATH_TOMCAT=/opt/tomcat-home;     TOMCAT_CHECKSUM="aaa2851bdc7a2476b6793e95174965c1c861531f161d8a138e87f8532b1af4d4b3d92dd1ae890614a692e5f13fb2e6946a1ada888f21e9d7db1964616b4181f0";     TOMCAT_DWNLD_URL="https://dlcdn.apache.org/tomcat/tomcat-9/v9.0.89/bin/apache-tomcat-9.0.89.tar.gz";         mkdir -p "${DOWNLOAD_PATH_TOMCAT}" "${INSTALL_PATH_TOMCAT}";     curl -LfsSo "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz "${TOMCAT_DWNLD_URL}";     echo "${TOMCAT_CHECKSUM} *${DOWNLOAD_PATH_TOMCAT}/tomcat.tar.gz" | sha512sum -c -;     tar -xf "${DOWNLOAD_PATH_TOMCAT}"/tomcat.tar.gz -C "${INSTALL_PATH_TOMCAT}" --strip-components=1;     rm -rf "${DOWNLOAD_PATH_TOMCAT}";         java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 15;     FULL=$( (java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     DST_CACHE=$(java -Xshareclasses:name=dry_run_scc,cacheDir=/opt/java/.scc,destroy 2>&1 || true);     SCC_SIZE=$(echo $SCC_SIZE | sed 's/.$//');     SCC_SIZE=$(awk "BEGIN {print int($SCC_SIZE * $FULL / 100.0)}");     [ "${SCC_SIZE}" -eq 0 ] && SCC_SIZE=1;     SCC_SIZE="${SCC_SIZE}m";     java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal,createLayer -Xscmx$SCC_SIZE -version;     unset OPENJ9_JAVA_OPTIONS;         export OPENJ9_JAVA_OPTIONS="-XX:+IProfileDuringStartupPhase -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,bootClassesOnly,nonFatal";     "${INSTALL_PATH_TOMCAT}"/bin/startup.sh;     sleep 5;     "${INSTALL_PATH_TOMCAT}"/bin/shutdown.sh -force;     sleep 5;     FULL=$( (java -Xshareclasses:name=openj9_system_scc,cacheDir=/opt/java/.scc,printallStats 2>&1 || true) | awk '/^Cache is [0-9.]*% .*full/ {print substr($3, 1, length($3)-1)}');     echo "SCC layer is $FULL% full.";     rm -rf "${INSTALL_PATH_TOMCAT}";     if [ -d "/opt/java/.scc" ]; then           chmod -R 0777 /opt/java/.scc;     fi;         echo "SCC generation phase completed"; # buildkit
```

-	Layers:
	-	`sha256:22512bbfe178a8ec7b5e4e48135f8a3e1ad0245ed3ee6a47f89947ce7ffb5d4f`  
		Last Modified: Mon, 03 Jun 2024 10:47:11 GMT  
		Size: 28.0 MB (28000515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7a4135208bd6a1c83ef4006ee13da7687af58d5df19772a183b62d4757a473`  
		Last Modified: Tue, 25 Jun 2024 23:02:32 GMT  
		Size: 12.2 MB (12203759 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7754a8ca2dce648029083ea974a21b6fd3906138a26b88630c882da49d22fc6`  
		Last Modified: Tue, 25 Jun 2024 23:21:37 GMT  
		Size: 54.9 MB (54945014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f253398902b5685c44eeee318e5451824737fecf56beb610919a11df86d97b5f`  
		Last Modified: Tue, 25 Jun 2024 23:21:36 GMT  
		Size: 5.2 MB (5227150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `ibm-semeru-runtimes:open-21.0.3_9-jre` - unknown; unknown

```console
$ docker pull ibm-semeru-runtimes@sha256:ddec6157fdd3d09a690d5d86f661ee70a72a98849362849301c8676b2f57b67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3459647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f9337ef13e207d2b497f1c93a1cafa82f710daf6d495be524e683f760ed3213`

```dockerfile
```

-	Layers:
	-	`sha256:2d06fb0e7228e502496dc9273a63faa409e0825a89845e823ea1be1f8c5fa08c`  
		Last Modified: Tue, 25 Jun 2024 23:21:35 GMT  
		Size: 3.4 MB (3435249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:def799f2ae35574d038391496fe78b2df11ec661570ce44f703a9e811ec9b809`  
		Last Modified: Tue, 25 Jun 2024 23:21:35 GMT  
		Size: 24.4 KB (24398 bytes)  
		MIME: application/vnd.in-toto+json
