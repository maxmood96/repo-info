## `eclipse-temurin:latest`

```console
$ docker pull eclipse-temurin@sha256:3f4c0f0440f9fae6b62a1477bcca263af5fda2baf819bfa03d3424433e9953de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `eclipse-temurin:latest` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:fbade3ae8db29689556eff27d0a59436e50fa4c566d4c89d3ed5e2ac283d78ff
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **206.5 MB (206542788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65015eb1fe2d80464ef206a401af9a6117cd626a78492fb8bf17913defc46e72`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 01 Dec 2023 07:49:48 GMT
ARG RELEASE
# Fri, 01 Dec 2023 07:49:48 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 01 Dec 2023 07:49:48 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 01 Dec 2023 07:49:50 GMT
ADD file:36d444e2cede3abe58191dcf28890b874c0908f5259bf7e8855338555701c4c5 in / 
# Fri, 01 Dec 2023 07:49:50 GMT
CMD ["/bin/bash"]
# Sat, 02 Dec 2023 01:58:08 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 01:58:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Dec 2023 01:58:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 02 Dec 2023 02:01:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Sat, 02 Dec 2023 02:01:53 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Sat, 02 Dec 2023 02:02:02 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e184dc29a6712c1f78754ab36fb48866583665fa345324f1a79e569c064f95e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1a6fa8abda4c5caed915cfbeeb176e7fbd12eb6b222f26e290ee45808b529aa1';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9574828ef3d735a25404ced82e09bf20e1614f7d6403956002de9cfbfcb8638f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Sat, 02 Dec 2023 02:02:05 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Sat, 02 Dec 2023 02:02:05 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Sat, 02 Dec 2023 02:02:05 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Sat, 02 Dec 2023 02:02:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:cbe3537751ce03ea42788c2fbe2d5d336180dc2e20472c8cdba8b3224191d101`  
		Last Modified: Wed, 29 Nov 2023 19:24:54 GMT  
		Size: 30.4 MB (30446322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cd63fc495d1a4839e5239c716fa5a6ec48209bff26db1e7d7af7b0701ac4ee7`  
		Last Modified: Sat, 02 Dec 2023 02:06:15 GMT  
		Size: 17.5 MB (17455452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6924fdd5c53e9e6a4f0905a3ae0632c92bdbffbbba857546a23871cef74265`  
		Last Modified: Sat, 02 Dec 2023 02:07:21 GMT  
		Size: 158.6 MB (158640107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be39ca79f5d28c28f3f2498ca0f67a9337066ea52acc98e8f3837b369bd32735`  
		Last Modified: Sat, 02 Dec 2023 02:07:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c878de00ef575697a60f792a5b79be9f2e74d8970e6d7e519088ea205bef7a57`  
		Last Modified: Sat, 02 Dec 2023 02:07:09 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:a662a9e3f0c43f87a36ebb3efc173df31df42d2053722d9b24b3a45377d2dfa5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.1 MB (204128878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ace42b0ccd35bfd01f935d0e7cc299c307854380dcb0f363421a38eac17f017`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Oct 2023 07:32:20 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:32:21 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:32:21 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:32:22 GMT
ADD file:f8594e26831508c318e42c8dfd9942041031087b8de1bf3fec11fd75b8b30fd4 in / 
# Thu, 05 Oct 2023 07:32:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 02:46:31 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 02:46:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 02:46:31 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:44:05 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:46:06 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Mon, 30 Oct 2023 23:46:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e184dc29a6712c1f78754ab36fb48866583665fa345324f1a79e569c064f95e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1a6fa8abda4c5caed915cfbeeb176e7fbd12eb6b222f26e290ee45808b529aa1';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9574828ef3d735a25404ced82e09bf20e1614f7d6403956002de9cfbfcb8638f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:46:17 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:46:17 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:46:17 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:46:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:895d322e8e5957c04af3ab7b3431f2a562182d34167c6e159e02044150a66967`  
		Last Modified: Thu, 05 Oct 2023 08:57:30 GMT  
		Size: 28.4 MB (28391939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f494a0917249ff640404cd9965fcd6a5ed5b7725fc21ff44518307f60c8e0a`  
		Last Modified: Mon, 30 Oct 2023 23:50:44 GMT  
		Size: 18.9 MB (18858788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b26a5f79e048ca492a5b8ac9d20968e30d614e9a674156d83ae0b8381f1df7`  
		Last Modified: Mon, 30 Oct 2023 23:53:19 GMT  
		Size: 156.9 MB (156877245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:759c5cde3e2f12b250b5ccdf6c694eabebe9b31e83c962a601ec7941560b68bd`  
		Last Modified: Mon, 30 Oct 2023 23:53:08 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b4da4cf0b7c631eb405738b2424f2e660232408f0b6a1087edf7ea5eea53bd6`  
		Last Modified: Mon, 30 Oct 2023 23:53:08 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - linux; ppc64le

```console
$ docker pull eclipse-temurin@sha256:d57e655834b4ea9eed05e11e1a4570a4baad68aa95b9ef3945e51f801612aaaa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **212.7 MB (212654116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7f3c98a3fdec05060e6268c0bdc3327e05af609114c791f8a4c0ca67798f45`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 05 Oct 2023 07:34:18 GMT
ARG RELEASE
# Thu, 05 Oct 2023 07:34:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 05 Oct 2023 07:34:19 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 05 Oct 2023 07:34:22 GMT
ADD file:595ff761b2778bdc6bb59cbe8ce51c4a247e0f279ccd59a17b5be6cdeac0b4d2 in / 
# Thu, 05 Oct 2023 07:34:22 GMT
CMD ["/bin/bash"]
# Fri, 13 Oct 2023 08:00:39 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 08:00:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 08:00:41 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:24:27 GMT
RUN set -eux;     apt-get update;     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends         curl         wget         fontconfig         ca-certificates p11-kit         binutils         tzdata         locales     ;     echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen;     locale-gen en_US.UTF-8;     rm -rf /var/lib/apt/lists/*
# Mon, 30 Oct 2023 23:27:16 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Mon, 30 Oct 2023 23:27:32 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='e184dc29a6712c1f78754ab36fb48866583665fa345324f1a79e569c064f95e9';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_aarch64_linux_hotspot_21.0.1_12.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='1a6fa8abda4c5caed915cfbeeb176e7fbd12eb6b222f26e290ee45808b529aa1';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_linux_hotspot_21.0.1_12.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='9574828ef3d735a25404ced82e09bf20e1614f7d6403956002de9cfbfcb8638f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_ppc64le_linux_hotspot_21.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget --progress=dot:giga -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Mon, 30 Oct 2023 23:27:37 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:27:37 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:27:37 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:27:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:589c4cce1daa100afadbdbeda96025d02f85c117e0e60b70801af41b4e618668`  
		Last Modified: Fri, 13 Oct 2023 06:13:20 GMT  
		Size: 35.7 MB (35682793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:494f75987917a46354a891e88bff3d330d2cb87ae470f00c3e4eb11c59000dc4`  
		Last Modified: Mon, 30 Oct 2023 23:32:42 GMT  
		Size: 18.7 MB (18724494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:614d17a41192beea6fd90d2b192dd2ff398c10afd7dd2e3f7703c34ae8bd4bd7`  
		Last Modified: Mon, 30 Oct 2023 23:35:21 GMT  
		Size: 158.2 MB (158245918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adcf4fcdda4dcab2af46e2c2dc3a757b577c346797d7f68c3e9a32a8d8b130b9`  
		Last Modified: Mon, 30 Oct 2023 23:35:06 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f823f2a5d3d29361637e89c4212356335911f8abe964374d5727c66501ba52b8`  
		Last Modified: Mon, 30 Oct 2023 23:35:06 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - windows version 10.0.20348.2113; amd64

```console
$ docker pull eclipse-temurin@sha256:f7dddcc153f693a90bb8e50308c561aa01c8ee413550cdef32dfa97de144669b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2267352934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a9a181715835bd8ce254b0fef43a632370f407c21d0965bd379bcf85f1112ea`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 01:36:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:07:02 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Thu, 16 Nov 2023 02:08:04 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_windows_hotspot_21.0.1_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_windows_hotspot_21.0.1_12.msi ;     Write-Host ('Verifying sha256 (62e12510b0097bd784b14b035013a32c65e7da334220c3ddfcc90d87440d240c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '62e12510b0097bd784b14b035013a32c65e7da334220c3ddfcc90d87440d240c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Nov 2023 02:08:27 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 16 Nov 2023 02:08:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fbeb193d02c2ca7f9a9ea438fbf1bcdb6ea4a6fea626713330fd1ebb514424f`  
		Last Modified: Thu, 16 Nov 2023 02:25:14 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440b81e15e6345fb78d7818811cb5c79584145ee0bf83b56a9896a4f62a4482e`  
		Last Modified: Thu, 16 Nov 2023 02:34:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10295762b34627491c93362a0d88709a0032cdf4084461dc6dbe1326f42f3b8e`  
		Last Modified: Thu, 16 Nov 2023 02:35:21 GMT  
		Size: 380.3 MB (380289093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a6c08bd3c3bc9dc812052abb448e267fbe30e1c8d5773fc105afcf7052bb79`  
		Last Modified: Thu, 16 Nov 2023 02:34:52 GMT  
		Size: 278.5 KB (278493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da8f9a9a507e8cdd5b3af0499a557b6917e3a559a6c6bfd13eaa2b3aa839dfe6`  
		Last Modified: Thu, 16 Nov 2023 02:34:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:latest` - windows version 10.0.17763.5122; amd64

```console
$ docker pull eclipse-temurin@sha256:8d6e3ac3d87b87caa15b2747115cdd81b545157776a9ec644d9ecc29efa770eb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2441730287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d0cd4357b5910d264abaa2666b42a1fa6a700994ec937239e1ffe9046c9409`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 01:37:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Nov 2023 02:08:45 GMT
ENV JAVA_VERSION=jdk-21.0.1+12
# Thu, 16 Nov 2023 02:10:28 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_windows_hotspot_21.0.1_12.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.1%2B12/OpenJDK21U-jdk_x64_windows_hotspot_21.0.1_12.msi ;     Write-Host ('Verifying sha256 (62e12510b0097bd784b14b035013a32c65e7da334220c3ddfcc90d87440d240c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '62e12510b0097bd784b14b035013a32c65e7da334220c3ddfcc90d87440d240c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Nov 2023 02:11:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 16 Nov 2023 02:11:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7a1cc914f0f5e059bfdf02906a6e052b1c97cebaf91eb6c2fd835cfddebda2`  
		Last Modified: Thu, 16 Nov 2023 02:26:46 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5bedd24dc32424e5fcae0643f511f84b138f4579bd55a9c29dfd2f2a54d92d`  
		Last Modified: Thu, 16 Nov 2023 02:35:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ae30561d12d374c3d7fbdaad84d0ccd77c70d6d4360b366a60dd010b76690c`  
		Last Modified: Thu, 16 Nov 2023 02:36:03 GMT  
		Size: 380.3 MB (380299112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78ed89e327f5392d03fd95bedec8442bac0062ca3e4b2f4801a30ad12339c782`  
		Last Modified: Thu, 16 Nov 2023 02:35:35 GMT  
		Size: 4.0 MB (3995489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d283f77e1cda65207b885f8e0d71f0dab4c9936ba1a22b822058b9a19e3bd0`  
		Last Modified: Thu, 16 Nov 2023 02:35:34 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
