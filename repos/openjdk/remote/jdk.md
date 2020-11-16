## `openjdk:jdk`

```console
$ docker pull openjdk@sha256:2e5241c6a2eacb50fff84f13ee3ba51bbc91ed3c5d8a3afb4a30a1946a7605a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1577; amd64
	-	windows version 10.0.14393.4046; amd64

### `openjdk:jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:06bd36ad06e052ea3ec0cc18c971a2e514d57c7a80764d9469dc86ecb650dc4d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251094936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f057dde245afb7b9289214141d669cb17ff21b99abad41ca0ffababf5833278`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Mon, 16 Nov 2020 19:37:29 GMT
ADD file:c6983fc83bb99ae9a8b343abf1e6852c64556f7c59e869f14f3f8835130d087d in / 
# Mon, 16 Nov 2020 19:37:29 GMT
CMD ["/bin/bash"]
# Mon, 16 Nov 2020 20:19:26 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 16 Nov 2020 20:19:26 GMT
ENV LANG=C.UTF-8
# Mon, 16 Nov 2020 20:20:31 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 16 Nov 2020 20:20:32 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Nov 2020 20:20:32 GMT
ENV JAVA_VERSION=15.0.1
# Mon, 16 Nov 2020 20:21:14 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 16 Nov 2020 20:21:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e69ec1c7b788c406991d1ce5f4a8f26a7ae9c0c9410d652237e2a6646ef53305`  
		Last Modified: Mon, 16 Nov 2020 19:38:51 GMT  
		Size: 42.1 MB (42053575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2259f1956e4980849285f91a1fd9fcc0f27002dddd076924e6801a2ae978db5a`  
		Last Modified: Mon, 16 Nov 2020 20:23:44 GMT  
		Size: 13.3 MB (13263119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b5c7ae0cae52fe2ca4367d2f66cd46ade0cedbbef429266f702a4ef4a8b4bb`  
		Last Modified: Mon, 16 Nov 2020 20:24:58 GMT  
		Size: 195.8 MB (195778242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:07156e86090a503e9a8a4a6293c684588a159fc8323bb94f507e51211ae3ace1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230930304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d15cf9375acadcc7a75936df60176e61edea1c43c3b5211edb4c459290545c44`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Mon, 16 Nov 2020 19:46:09 GMT
ADD file:91f2f5092142d551bd5542d693b0d6f9d6f9de47a18e19492b8db9dd24ef0786 in / 
# Mon, 16 Nov 2020 19:46:11 GMT
CMD ["/bin/bash"]
# Mon, 16 Nov 2020 20:04:04 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 16 Nov 2020 20:04:05 GMT
ENV LANG=C.UTF-8
# Mon, 16 Nov 2020 20:04:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Mon, 16 Nov 2020 20:04:56 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Nov 2020 20:04:57 GMT
ENV JAVA_VERSION=15.0.1
# Mon, 16 Nov 2020 20:05:32 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Mon, 16 Nov 2020 20:05:34 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:74c8bc77d8380334fed77b152e6228e91ad4e881fb67a762337f88c14031e719`  
		Last Modified: Mon, 16 Nov 2020 19:47:43 GMT  
		Size: 42.0 MB (41982578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b01f480947edbfcab3306d055a8959aa86cba86597ea1e29c498fa3fd689e7e4`  
		Last Modified: Mon, 16 Nov 2020 20:08:26 GMT  
		Size: 14.1 MB (14060251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6e98a2b7b4dbf76fa2199daa71043c6f525bb5079d2816332adcc87670e7b2`  
		Last Modified: Mon, 16 Nov 2020 20:10:29 GMT  
		Size: 174.9 MB (174887475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:jdk` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:cc19357fbf820dc526ca018066b77a5bc8d6a772ac212931edfe9181dc8f336b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2593691442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0226176cf45adca5db62c625fbecb82b09d63019d0b4d3adf089b1a6087e8b55`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 03 Nov 2020 03:11:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Nov 2020 13:26:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 17:45:35 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Nov 2020 17:54:42 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 11 Nov 2020 17:55:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Nov 2020 17:55:05 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 11 Nov 2020 17:55:06 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_windows-x64_bin.zip
# Wed, 11 Nov 2020 17:55:06 GMT
ENV JAVA_SHA256=0a27c733fc7ceaaae3856a9c03f5e2304af30a32de6b454b8762ec02447c5464
# Wed, 11 Nov 2020 17:56:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Nov 2020 17:56:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680bbdbacf1bcbace70de5087d02d31e9dd7a22feae59f746f54dab46c1d5bda`  
		Size: 669.7 MB (669696346 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da5a67a9f3a363cb69c8104913a5a58c1c47e8f648a07d057fc28a5f98790e60`  
		Last Modified: Wed, 11 Nov 2020 13:37:50 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bee39b5545a888688525644d5ac139bf90e9e5031cc78ac03612316b125116`  
		Last Modified: Wed, 11 Nov 2020 18:25:54 GMT  
		Size: 9.2 MB (9240273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0973c59936732eedabd3b53ae0d93d7b6d85e2bee99be168d3e32fda2c839ed2`  
		Last Modified: Wed, 11 Nov 2020 18:28:18 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d185147d2adada72deeee874831866f57b4eca71460d8f32a1f46bd296ddce0`  
		Last Modified: Wed, 11 Nov 2020 18:28:18 GMT  
		Size: 307.2 KB (307205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb39f4c713d78cd1b14f256756f09dce1cf1a036b2def1604c35306920fcafa`  
		Last Modified: Wed, 11 Nov 2020 18:28:15 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d96399de34afbf27db837d06f9c05d0df294668e29cd35297b34a12029722262`  
		Last Modified: Wed, 11 Nov 2020 18:28:15 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8ea21a6235519d5f86025520d6be5148ee744a8f64407f65d241dd48d6c15f`  
		Last Modified: Wed, 11 Nov 2020 18:28:16 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2099a8d1b04e554651318e8ace9d9b4ec09081c50584c45ca6911e0d707b604e`  
		Last Modified: Wed, 11 Nov 2020 18:28:35 GMT  
		Size: 196.1 MB (196107850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:881564af5829291ccf4bdb298eca81973ce2902f4fadac2f3755456fe541e842`  
		Last Modified: Wed, 11 Nov 2020 18:28:15 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:jdk` - windows version 10.0.14393.4046; amd64

```console
$ docker pull openjdk@sha256:f0c1de9259745d085481a3201b9093205afc4d7d719f45f4fcc021767642a542
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5987600348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fec181511021a17fca96947ab6d09105f869dd89864ce19bb4e8aa9b680b94e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 17:49:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Nov 2020 17:56:57 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 11 Nov 2020 17:58:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 11 Nov 2020 17:58:08 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 11 Nov 2020 17:58:09 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_windows-x64_bin.zip
# Wed, 11 Nov 2020 17:58:10 GMT
ENV JAVA_SHA256=0a27c733fc7ceaaae3856a9c03f5e2304af30a32de6b454b8762ec02447c5464
# Wed, 11 Nov 2020 18:01:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Nov 2020 18:01:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1222181efe25bb0d500f320707eb7dc24e576749c0897042ae1f3b8116e87990`  
		Last Modified: Wed, 11 Nov 2020 18:26:42 GMT  
		Size: 10.1 MB (10078764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4801e331f33400c78cbca4fa2d31ce1f3d8be339b35c071a94fdfa6b1dba70`  
		Last Modified: Wed, 11 Nov 2020 18:29:10 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39699ad7da98d3d5df78c9f6f50d1cfce2c3642acce10777a447acaf906934c2`  
		Last Modified: Wed, 11 Nov 2020 18:29:10 GMT  
		Size: 5.5 MB (5511740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd2a2f40a57c964942f61b748ef85db667666de3a769a027825b710f14ca742`  
		Last Modified: Wed, 11 Nov 2020 18:29:05 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4aa890aa6dc9e04b3c1630325aa4ca9416a6c379fb0b3f33458bc484be350a7`  
		Last Modified: Wed, 11 Nov 2020 18:29:05 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35aed1d674b0116bb80c6a81f2b772a04384831348be9e8eeab2a03058ab6a12`  
		Last Modified: Wed, 11 Nov 2020 18:29:07 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56629434f764f24aa26f82b211ec5da5507c2e7052366bd0dfc62f8d1c15e25`  
		Last Modified: Wed, 11 Nov 2020 18:29:28 GMT  
		Size: 201.4 MB (201444075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96577d60ea0843b82c7799f6ec91393381657d21dd7ebe31bbb457fd79ab8a22`  
		Last Modified: Wed, 11 Nov 2020 18:29:06 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
