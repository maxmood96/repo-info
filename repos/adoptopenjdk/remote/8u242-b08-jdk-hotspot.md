## `adoptopenjdk:8u242-b08-jdk-hotspot`

```console
$ docker pull adoptopenjdk@sha256:b08de63f2d9a078b9280bbf8fb0d3692c951260f12f5b3327cb5da377f5479d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; arm64 variant v8
	-	windows version 10.0.14393.3506; amd64
	-	windows version 10.0.17763.1040; amd64

### `adoptopenjdk:8u242-b08-jdk-hotspot` - linux; arm64 variant v8

```console
$ docker pull adoptopenjdk@sha256:b59cc63270f5440d1d1c38b24ea49435df58580daf2d1d06c7f5a9996061c429
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141761555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3f23f1cdb51407a5b2cb502f6d0e8bdb3d510c06ed68c69a2bf8885a583bc36`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Feb 2020 21:54:16 GMT
ADD file:d827a0b8f08011678a718254c1220408c7e6c7ab03ae4259b415542309f18578 in / 
# Fri, 21 Feb 2020 21:54:21 GMT
RUN [ -z "$(apt-get indextargets)" ]
# Fri, 21 Feb 2020 21:54:23 GMT
RUN set -xe 		&& echo '#!/bin/sh' > /usr/sbin/policy-rc.d 	&& echo 'exit 101' >> /usr/sbin/policy-rc.d 	&& chmod +x /usr/sbin/policy-rc.d 		&& dpkg-divert --local --rename --add /sbin/initctl 	&& cp -a /usr/sbin/policy-rc.d /sbin/initctl 	&& sed -i 's/^exit.*/exit 0/' /sbin/initctl 		&& echo 'force-unsafe-io' > /etc/dpkg/dpkg.cfg.d/docker-apt-speedup 		&& echo 'DPkg::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' > /etc/apt/apt.conf.d/docker-clean 	&& echo 'APT::Update::Post-Invoke { "rm -f /var/cache/apt/archives/*.deb /var/cache/apt/archives/partial/*.deb /var/cache/apt/*.bin || true"; };' >> /etc/apt/apt.conf.d/docker-clean 	&& echo 'Dir::Cache::pkgcache ""; Dir::Cache::srcpkgcache "";' >> /etc/apt/apt.conf.d/docker-clean 		&& echo 'Acquire::Languages "none";' > /etc/apt/apt.conf.d/docker-no-languages 		&& echo 'Acquire::GzipIndexes "true"; Acquire::CompressionTypes::Order:: "gz";' > /etc/apt/apt.conf.d/docker-gzip-indexes 		&& echo 'Apt::AutoRemove::SuggestsImportant "false";' > /etc/apt/apt.conf.d/docker-autoremove-suggests
# Fri, 21 Feb 2020 21:54:25 GMT
RUN mkdir -p /run/systemd && echo 'docker' > /run/systemd/container
# Fri, 21 Feb 2020 21:54:25 GMT
CMD ["/bin/bash"]
# Fri, 21 Feb 2020 22:41:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 21 Feb 2020 22:42:11 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Thu, 27 Feb 2020 04:50:34 GMT
ENV JAVA_VERSION=jdk8u242-b08
# Thu, 27 Feb 2020 04:51:08 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a2314de7f0120c9bdc69aec2198428a2deeb9ad977fc6801f89d0ec8382d65a5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_jdk8u242-b08.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='72f42c2014cb29a2fcd71b1a678af3ed148358a8f9b7d741a5da88cb178d9c53';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u242b08.tar.gz';          ;;        s390x)          ESUM='98f7217dc4acc6bc8b474a2009922b51767d84c045f95a16ee0b9216467ba2de';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_s390x_linux_hotspot_8u242b08.tar.gz';          ;;        amd64|x86_64)          ESUM='f39b523c724d0e0047d238eb2bb17a9565a60574cf651206c867ee5fc000ab43';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u242b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 27 Feb 2020 04:51:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:6695dc10aaa5cd71c433dfb366e84804eb5fbee91eab1e113442040d6ef4c9e0`  
		Last Modified: Fri, 21 Feb 2020 21:56:13 GMT  
		Size: 23.7 MB (23721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aab8f928deff72c9b5867c93524a60e3f8cf1b7401c88b0ede8dc3c595e828`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 35.2 KB (35197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e83b6447acdea2afff1a10052ebc551d15bfd1d2a93a202699f7a458c612c07`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 850.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6a91485a919c412d218b6441c339f691079ff88e6d28734b1cc3d5938cf58d`  
		Last Modified: Fri, 21 Feb 2020 21:56:08 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0b5eadacd92003b0f840ccaa2c2b09ea51d298126dd647d280a6de60720a3d4`  
		Last Modified: Fri, 21 Feb 2020 22:44:36 GMT  
		Size: 12.7 MB (12732441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8b9cfb7a6b11243aa95d0ba52bab0351e389053a2d88b4b69eab6cebcb3f04`  
		Last Modified: Thu, 27 Feb 2020 04:52:42 GMT  
		Size: 105.3 MB (105271735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u242-b08-jdk-hotspot` - windows version 10.0.14393.3506; amd64

```console
$ docker pull adoptopenjdk@sha256:fea7370dec28df04b081bec2cfd4f0363b97b03a3367b8171164575af6b6c138
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5926571656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b69c462410593eb17e33d18e7768e190e087e88e24b9ca5e062934b1177a906b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 01:48:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 26 Feb 2020 23:15:17 GMT
ENV JAVA_VERSION=jdk8u242-b08
# Wed, 26 Feb 2020 23:18:12 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u242b08.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u242b08.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (10478f65692b86bfff4fc029db119d6eac2a48f23c1bc542e5443ce6f2547573) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '10478f65692b86bfff4fc029db119d6eac2a48f23c1bc542e5443ce6f2547573') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:72c4471958f7f0f07260f0f430bcffb0bc07811088c24cffba1439d250ea1ae3`  
		Last Modified: Thu, 20 Feb 2020 03:04:52 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdaf4b2a0af020d8d06062c1be67e1e89f1c407f937a85fb12fc8f5d68c29614`  
		Last Modified: Wed, 26 Feb 2020 23:28:09 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bfcdfb0791c9dd8ac1b035dc0d8cac981d61a211448cab099a23611aa6c1c8`  
		Last Modified: Wed, 26 Feb 2020 23:28:35 GMT  
		Size: 199.5 MB (199504260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u242-b08-jdk-hotspot` - windows version 10.0.17763.1040; amd64

```console
$ docker pull adoptopenjdk@sha256:3f66fbdf1e5d08e8d1312f6147073cb87dbb7aa270d8254305b413f09970bb86
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2429203205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff713c957fe561119b22930b7779feddb94651aedcaa6c2d4cdc427fe3ef236`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 26 Feb 2020 23:18:38 GMT
ENV JAVA_VERSION=jdk8u242-b08
# Wed, 26 Feb 2020 23:20:47 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u242b08.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u242b08.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (10478f65692b86bfff4fc029db119d6eac2a48f23c1bc542e5443ce6f2547573) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '10478f65692b86bfff4fc029db119d6eac2a48f23c1bc542e5443ce6f2547573') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7436f30ab01dd622ba1ef52f7da17d6c580132e1352986654a6d40a0d66a60ee`  
		Last Modified: Wed, 26 Feb 2020 23:29:26 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe616447bf282f8b3e9dba9f2087f9f8bd44980abf36ec9a7efc5b78d643a880`  
		Last Modified: Wed, 26 Feb 2020 23:29:49 GMT  
		Size: 198.7 MB (198696905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
