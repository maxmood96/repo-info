## `openjdk:15-jdk`

```console
$ docker pull openjdk@sha256:3ee42b89555f1563024c10132dda0693be1f14145f46de5d0e6151628e82b5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `openjdk:15-jdk` - linux; amd64

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

### `openjdk:15-jdk` - linux; arm64 variant v8

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

### `openjdk:15-jdk` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:d2468598629140cb30edf61eedd304c755deb7d4bd982077090819e97cff29d6
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2596492998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f37ab6461dcc58344f708e17cafe67983977172a0b7688358e65cb19dc2f70`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 18:50:31 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 09 Dec 2020 18:59:49 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 09 Dec 2020 19:00:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 09 Dec 2020 19:00:10 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 09 Dec 2020 19:00:11 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_windows-x64_bin.zip
# Wed, 09 Dec 2020 19:00:12 GMT
ENV JAVA_SHA256=0a27c733fc7ceaaae3856a9c03f5e2304af30a32de6b454b8762ec02447c5464
# Wed, 09 Dec 2020 19:02:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 19:02:02 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935e3005fe76a11e222d9322d452d314edc4ba767499cc7c7e9f7cff154513fc`  
		Last Modified: Wed, 09 Dec 2020 19:32:28 GMT  
		Size: 9.2 MB (9236222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bf3750bea96f7ea8b6aa19ff70ed12a705d91d16dcc1fb5a3c85f5730f5344`  
		Last Modified: Wed, 09 Dec 2020 19:34:46 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90942bd8683cbd3eef336f8314d215359de32f896e8e2efbeb1f697e0ff9c44`  
		Last Modified: Wed, 09 Dec 2020 19:34:46 GMT  
		Size: 288.8 KB (288801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ff7b63af5b94beea5760459ffac1b1967daa2c9780e5eb2eb77b8d8aa15ba67`  
		Last Modified: Wed, 09 Dec 2020 19:34:43 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915603362ace290ac140d8453a67924acb5ac93097c101c4344c37ee9af7adfa`  
		Last Modified: Wed, 09 Dec 2020 19:34:43 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e2a285389d2f3c56f58a06b3ebf54c6bc94c1673186494b25aca1802fa3ab4`  
		Last Modified: Wed, 09 Dec 2020 19:34:43 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b0bcfd3149e1d06b243441dcaaf06c6a28b2159c8b1e06cd03a19aee888f5a`  
		Last Modified: Wed, 09 Dec 2020 19:35:04 GMT  
		Size: 196.1 MB (196086698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5467d9ebf6c327b0799032c39ffe0264afde65a86c4fa0fd9aa2501acf2fcb`  
		Last Modified: Wed, 09 Dec 2020 19:34:43 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-jdk` - windows version 10.0.14393.4104; amd64

```console
$ docker pull openjdk@sha256:15851515876d43373b4351f1c81d77cd1837af7329f17c9a6ac4f8fe149238bf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5985773335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72ade9930cb1d311d30d1677ffdd2dc42e8ef83165c1be1fb2cfebd0546e899b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 13:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 18:53:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 09 Dec 2020 19:02:15 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 09 Dec 2020 19:03:27 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 09 Dec 2020 19:03:27 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 09 Dec 2020 19:03:28 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_windows-x64_bin.zip
# Wed, 09 Dec 2020 19:03:29 GMT
ENV JAVA_SHA256=0a27c733fc7ceaaae3856a9c03f5e2304af30a32de6b454b8762ec02447c5464
# Wed, 09 Dec 2020 19:05:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 19:05:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c6d005eb9e78ad42f77f3dad7e29d954e78f0547f9884fe024a71f4042412970`  
		Last Modified: Wed, 09 Dec 2020 13:55:31 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:535454b21129910f68c2c2c0ef15ca3640eb529cf7325adda5148aa9a68bc914`  
		Last Modified: Wed, 09 Dec 2020 19:33:19 GMT  
		Size: 10.0 MB (10046782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84203973860ac0ffdd9c4f9b547f104c63f16c0b03d178efbd770d2b08c05a25`  
		Last Modified: Wed, 09 Dec 2020 19:35:39 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e71876776f65fe3e65cf42cedf4fcd1bc449c2c66be3114f2ee54fe2915de6`  
		Last Modified: Wed, 09 Dec 2020 19:35:40 GMT  
		Size: 5.5 MB (5488263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c855d05e95620dce2f14bca23ce7d449384857b5f5904660caa384cc8ca86c`  
		Last Modified: Wed, 09 Dec 2020 19:35:35 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3b4b5b58a00512f18189b93e321ff1ce4afe59ecc4591b7c32bfa34415b85a`  
		Last Modified: Wed, 09 Dec 2020 19:35:35 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76db0dae0089a80377f7b851fd9e2466f5c8d2b6e16d3356791b85e4d3dff4eb`  
		Last Modified: Wed, 09 Dec 2020 19:35:36 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b07551fb0933b9b0743ef4c34a161d3e131b6843c6fa2464db4fa062a7883960`  
		Last Modified: Wed, 09 Dec 2020 19:35:58 GMT  
		Size: 201.4 MB (201387350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177dd40954599c4e6b034e257d3f7d4b92328673c7c35588fe36d9a921b39f62`  
		Last Modified: Wed, 09 Dec 2020 19:35:35 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
