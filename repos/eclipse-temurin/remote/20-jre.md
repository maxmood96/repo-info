## `eclipse-temurin:20-jre`

```console
$ docker pull eclipse-temurin@sha256:96b14269f6f9b53306ad96789055ed1a1dbe28637077e77811c6b6e96130c73d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1970; amd64
	-	windows version 10.0.17763.4851; amd64

### `eclipse-temurin:20-jre` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:db32cb29a978fa782ef97bf3a39f4955295712ebff305839c3faaf64f5c5b22b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **98.2 MB (98198687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b771c7b28c00f77d670bb68d2a763ab7713c6528feeb3b4d5fc22fd1f292d23f`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:05 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:05 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:05 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:07 GMT
ADD file:194c886b88876c1804cc5f80719669653c16a388b664147b7f22402105f533c4 in / 
# Mon, 25 Sep 2023 10:17:08 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 05:11:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 05:11:45 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 05:11:45 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 05:13:30 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 05:14:11 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Tue, 03 Oct 2023 05:14:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63a730d5a3b6d21d31f7cba15dc44b019a8a4d8652e13acec45040f98584112c';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_aarch64_linux_hotspot_20.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e3592e86290c192804d9c6b5035d42cc32cf04141d1c0b9d1ecb67739826c8c5';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 05:14:38 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 05:14:39 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 05:14:39 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:707e32e9fc569fee476af9e92ae3d1df8b8e6dca47f9cb31db9d2c922a6de952`  
		Last Modified: Mon, 25 Sep 2023 12:54:05 GMT  
		Size: 30.4 MB (30440869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e560b9ae2a605cbabd174647e334b0807409ab4cdb14e3ffa28655f8e033811`  
		Last Modified: Tue, 03 Oct 2023 05:17:36 GMT  
		Size: 17.5 MB (17455429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf40dd63c7361ad09281233aeba9b51a0c71e764891babcf957fc5c1cb479c5`  
		Last Modified: Tue, 03 Oct 2023 05:18:52 GMT  
		Size: 50.3 MB (50301496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25222345e662e88bfaed1142cb2283c23d7a30b89282c5931fe33430bf3e0b3`  
		Last Modified: Tue, 03 Oct 2023 05:18:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d4c0fe5879e719e58464a88d92bd1e872c67a41833d478b28df97a35c0aaaa`  
		Last Modified: Tue, 03 Oct 2023 05:18:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jre` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:0f9b4f25acf102da0aecee1e5771f6a1c26a26141e4158c4d2aa682c12547c21
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **96.8 MB (96765451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c663b87af7420c1208793a3f0bc226b410b869b0e29d3199b3436a965e7e09`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 25 Sep 2023 10:17:41 GMT
ARG RELEASE
# Mon, 25 Sep 2023 10:17:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 25 Sep 2023 10:17:41 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 25 Sep 2023 10:17:44 GMT
ADD file:8540670760767f19eaf101fbce1da1881a2f24a7d65da6abdedc644b8fb00463 in / 
# Mon, 25 Sep 2023 10:17:45 GMT
CMD ["/bin/bash"]
# Tue, 03 Oct 2023 06:06:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 06:06:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 06:06:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 03 Oct 2023 06:08:16 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales p11-kit binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 03 Oct 2023 06:08:48 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Tue, 03 Oct 2023 06:09:10 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='63a730d5a3b6d21d31f7cba15dc44b019a8a4d8652e13acec45040f98584112c';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_aarch64_linux_hotspot_20.0.2_9.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='e3592e86290c192804d9c6b5035d42cc32cf04141d1c0b9d1ecb67739826c8c5';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 03 Oct 2023 06:09:11 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Tue, 03 Oct 2023 06:09:11 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Tue, 03 Oct 2023 06:09:11 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:6ea603f1df5e3d23206761eca19fba4cdf4e22d773256cb65b71b730aa5acced`  
		Last Modified: Mon, 25 Sep 2023 17:30:11 GMT  
		Size: 28.4 MB (28392073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ba2aefbab3334adfc4bfa89dd448c89bc452ab89a02053172fb42a8e5288ba3`  
		Last Modified: Tue, 03 Oct 2023 06:11:30 GMT  
		Size: 18.9 MB (18859718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f12367f5a9d559b42ab65aa9579ff6ce6e4813a46d2a6e117d0bb17c3568ca6`  
		Last Modified: Tue, 03 Oct 2023 06:12:37 GMT  
		Size: 49.5 MB (49512769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f902fc9820f256fa2abfaad58a8c055be9ebc768898362ff5935860d5d4eca60`  
		Last Modified: Tue, 03 Oct 2023 06:12:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02235288b81548721328ae8dbde4f8abff594845486b012c8c07278f4e89f41d`  
		Last Modified: Tue, 03 Oct 2023 06:12:31 GMT  
		Size: 732.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jre` - windows version 10.0.20348.1970; amd64

```console
$ docker pull eclipse-temurin@sha256:cf10a8c8f399c9c68d71c03e565b716d9069032533c3316f3dfe5894e69ae37d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1916226589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e672839ad88fb0bb0e23114d837ef628c0436d0887153531ecb9291be03a6888`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 01 Sep 2023 00:43:48 GMT
RUN Install update 10.0.20348.1970
# Wed, 13 Sep 2023 01:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 03:05:59 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 03:13:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_windows_hotspot_20.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_windows_hotspot_20.0.2_9.msi ;     Write-Host ('Verifying sha256 (0217ba025c5ac579982a80791d4637e2b4b6afb14de522fff2b818d0203d4cea) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '0217ba025c5ac579982a80791d4637e2b4b6afb14de522fff2b818d0203d4cea') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 13 Sep 2023 03:14:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feca8e06011ab171ad74cda49c7c305e791965aef283d5b7c2b987dd5388e6c7`  
		Last Modified: Tue, 12 Sep 2023 18:24:42 GMT  
		Size: 448.7 MB (448675362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f40969dbf1e035a6c49e7c40b216960e3ee98ec3b76f76f9fe4498d0110bee`  
		Last Modified: Wed, 13 Sep 2023 02:15:22 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45487e7e73ad14f9d8b091ba267fce3cd52aa486492e242fab18a9edfb186d07`  
		Last Modified: Wed, 13 Sep 2023 03:43:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d4c3134c43088af35ff14001d6cd151bdf7df88f90ba7868aaac8f261e66ca9`  
		Last Modified: Wed, 13 Sep 2023 03:46:12 GMT  
		Size: 78.7 MB (78661629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212b1b29758cea959d60fa2c22d68e725c27bc160441d7e69858ee9968a0b81b`  
		Last Modified: Wed, 13 Sep 2023 03:46:00 GMT  
		Size: 288.1 KB (288091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jre` - windows version 10.0.17763.4851; amd64

```console
$ docker pull eclipse-temurin@sha256:c046ce08cb45925fa1cd647946692c91a7bb96ff4c742ae2c6b5f2c834f00004
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098307020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f35bb6f35977dee8e60a91c2d974ade59433870cffc8ce3c39b8c4232ebb0132`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 29 Aug 2023 17:09:18 GMT
RUN Install update 10.0.17763.4851
# Wed, 13 Sep 2023 01:39:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 03:08:12 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Wed, 13 Sep 2023 03:16:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_windows_hotspot_20.0.2_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_windows_hotspot_20.0.2_9.msi ;     Write-Host ('Verifying sha256 (0217ba025c5ac579982a80791d4637e2b4b6afb14de522fff2b818d0203d4cea) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '0217ba025c5ac579982a80791d4637e2b4b6afb14de522fff2b818d0203d4cea') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 13 Sep 2023 03:18:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179757339e051b99f9a62375fed8f87ffcc4df0eeedb984d20b485bdd089ad08`  
		Last Modified: Tue, 12 Sep 2023 19:41:25 GMT  
		Size: 365.7 MB (365709508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc14cbf6230cebb55cabf885ef8606e63f571dd05f37d899d95bca34972a44a`  
		Last Modified: Wed, 13 Sep 2023 02:16:50 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e0110e06f9a18136daf295b1af48ee11ec7e1a66ca481861aec4792e39db11`  
		Last Modified: Wed, 13 Sep 2023 03:44:40 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7e39347c2b94f7f83a5847f69acc9d80b24d2b1c52705f95c66a34da5420110`  
		Last Modified: Wed, 13 Sep 2023 03:46:33 GMT  
		Size: 78.7 MB (78682802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f28d493663129ec6012b9b7847a8486c4195f724a869bc001f767a884bc5764c`  
		Last Modified: Wed, 13 Sep 2023 03:46:22 GMT  
		Size: 3.3 MB (3291512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
