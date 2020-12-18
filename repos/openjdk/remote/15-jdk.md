## `openjdk:15-jdk`

```console
$ docker pull openjdk@sha256:53941e9d89421c4aa85fa8f1fb22e1d5ae4697d385baa2e269fe6502b5eff591
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `openjdk:15-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:02f6b131fbb5a7438e4d5bf8a06317b746c91c8e9d5a75be4d3cec8b69ae498a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **251.1 MB (251099194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e105e26a0a75a33b9a68b0a4080b71bff16ac595ca072fdc901da9adfbc8fbf4`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 21:22:07 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-amd64/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Fri, 18 Dec 2020 18:20:53 GMT
ADD file:ae640751036e8faf191ef80903201a939fb88b6280ec402d34f100cf54e41b5d in / 
# Fri, 18 Dec 2020 18:20:53 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 18:38:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 18 Dec 2020 18:38:18 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 18:39:22 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 18 Dec 2020 18:39:23 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Dec 2020 18:39:23 GMT
ENV JAVA_VERSION=15.0.1
# Fri, 18 Dec 2020 18:39:59 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 18 Dec 2020 18:39:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:edcbc9047efe2641ebc4f2393b0e5717733c062c211b0db349abc2ea82364e57`  
		Last Modified: Fri, 18 Dec 2020 18:22:18 GMT  
		Size: 42.1 MB (42059283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096c31e209d76bfb493c22693ffe401d20bd3b9b8bc2256934fda17f29780bb3`  
		Last Modified: Fri, 18 Dec 2020 18:42:59 GMT  
		Size: 13.3 MB (13261719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e211f51e5c4fddad313a905a3c938d804492f4a74fd37ff59f879d8238ecccd`  
		Last Modified: Fri, 18 Dec 2020 18:44:02 GMT  
		Size: 195.8 MB (195778192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:15-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:928b42f539b1556f6d3f0b0f7b57a43cfca52af9c53592588c00d8e7890514ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.9 MB (230932294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9145794983aa93b7f92e9073aecd114341dab06f380faebf0f44d42afc25e3b`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 15 Sep 2020 20:40:54 GMT
LABEL org.opencontainers.image.authors=Oracle Linux Product Team <ol-ovm-info_ww@oracle.com> org.opencontainers.image.url=https://github.com/oracle/container-images org.opencontainers.image.source=https://github.com/oracle/container-images/tree/dist-arm64v8/8-slim org.opencontainers.image.vendor=Oracle America, Inc org.opencontainers.image.title=Oracle Linux 8 (slim) org.opencontainers.image.description=Oracle Linux is an open-source       operating system available under the GNU General Public License (GPLv2) and       is suitable for both general purpose or Oracle workloads.
# Fri, 18 Dec 2020 18:43:40 GMT
ADD file:be2d17640c58ed7d6ce818b679805972eedbbacd4ab5ae5e15f5c8542d1ff8ea in / 
# Fri, 18 Dec 2020 18:43:43 GMT
CMD ["/bin/bash"]
# Fri, 18 Dec 2020 19:43:59 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 18 Dec 2020 19:43:59 GMT
ENV LANG=C.UTF-8
# Fri, 18 Dec 2020 19:47:44 GMT
ENV JAVA_HOME=/usr/java/openjdk-15
# Fri, 18 Dec 2020 19:47:45 GMT
ENV PATH=/usr/java/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Dec 2020 19:47:45 GMT
ENV JAVA_VERSION=15.0.1
# Fri, 18 Dec 2020 19:48:11 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-aarch64_bin.tar.gz; 			downloadSha256=6a62b7ec065280bad978a3322733a089153dec5ebf5ba81fd2fa361382dbc7b0; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_linux-x64_bin.tar.gz; 			downloadSha256=83ec3a7b1649a6b31e021cde1e58ab447b07fb8173489f27f427e731c89ed84a; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 18 Dec 2020 19:48:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:68012513ce8f557e79d400caae7326eb282a43c35afa4fd0a04e0c6470a0c6da`  
		Last Modified: Fri, 18 Dec 2020 18:45:16 GMT  
		Size: 42.0 MB (41984474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19435fd29840d5adb1fcf43416b769187aa10d3f70e390e22cd1edadb7415d63`  
		Last Modified: Fri, 18 Dec 2020 19:51:11 GMT  
		Size: 14.1 MB (14059908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eacb927968b99c3905c97438bc58feab590487875a20ae3a6815878a62425957`  
		Last Modified: Fri, 18 Dec 2020 19:55:03 GMT  
		Size: 174.9 MB (174887912 bytes)  
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
