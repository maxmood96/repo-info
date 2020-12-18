## `openjdk:16-jdk`

```console
$ docker pull openjdk@sha256:cfce8dd7f9d84e494d285321c9e53aa562b69a41bb6270ebf37cff14a429b765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `openjdk:16-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:8d2c4ff247e3aa31d993e0d7668b2c561ca316c432f7eacd0d2d1eb8fa947e8f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.2 MB (240157482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0321d4f631ce7c7138fb3695c5b566a9356fb00860e927bd968da652fd4c1111`
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
# Fri, 18 Dec 2020 18:38:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 18 Dec 2020 18:38:19 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Dec 2020 18:38:19 GMT
ENV JAVA_VERSION=16-ea+28
# Fri, 18 Dec 2020 18:38:53 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/28/GPL/openjdk-16-ea+28_linux-aarch64_bin.tar.gz; 			downloadSha256=ec5240a695751612960e7459476c6081e69a03aebe4ff3c7ae964b9235dfe9a4; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/28/GPL/openjdk-16-ea+28_linux-x64_bin.tar.gz; 			downloadSha256=2c2f2136a72e53deedef4e4e35d3d34315093a16732b9d112297e11e0661ea05; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 18 Dec 2020 18:38:53 GMT
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
	-	`sha256:98c0699868271b0128fd10926ce17b033a3341ceafd29c743438409af6ee0ee2`  
		Last Modified: Fri, 18 Dec 2020 18:43:13 GMT  
		Size: 184.8 MB (184836480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:424623fb8a4cb8d0b074e795684e2d7b06de52934c5d2976de2c39ea63c4208d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235247329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f4836247a7f9a97e2db55a152c2d7b28a3028d2adc7b1822074aaa6ee1c3ee6`
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
# Fri, 18 Dec 2020 19:44:00 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 18 Dec 2020 19:44:01 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Dec 2020 19:44:01 GMT
ENV JAVA_VERSION=16-ea+29
# Fri, 18 Dec 2020 19:44:43 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/29/GPL/openjdk-16-ea+29_linux-aarch64_bin.tar.gz; 			downloadSha256=2a273d305f8c5ed1eec0cec322ed37660eddd7bcf1b381583e6c6b66fe020eda; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/29/GPL/openjdk-16-ea+29_linux-x64_bin.tar.gz; 			downloadSha256=484b901cea7c2b6fafea3a4215028f12f225c17807d5413a2d52edcd604ef6ec; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 18 Dec 2020 19:44:45 GMT
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
	-	`sha256:fa8943f4ade502129912565fc904075ebbcf20da82a5faba818fe75c19898e4b`  
		Last Modified: Fri, 18 Dec 2020 19:51:34 GMT  
		Size: 179.2 MB (179202947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-jdk` - windows version 10.0.17763.1637; amd64

```console
$ docker pull openjdk@sha256:6ad2aea49efe921c742e8e6afa08d4baf78f68f4df7395f38f7f4ba1b96fd120
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2585258431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2e17c6f738aa3adab45b9634054df317fa432b03ef2e8353f35c5330e29dac0`
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
# Wed, 09 Dec 2020 18:50:32 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 09 Dec 2020 18:50:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 14 Dec 2020 21:24:37 GMT
ENV JAVA_VERSION=16-ea+28
# Mon, 14 Dec 2020 21:24:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/28/GPL/openjdk-16-ea+28_windows-x64_bin.zip
# Mon, 14 Dec 2020 21:24:39 GMT
ENV JAVA_SHA256=501d49c571b04ef0817887c975cc3a24ddd839acd752852e23312d0d8752e270
# Mon, 14 Dec 2020 21:26:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Dec 2020 21:26:23 GMT
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
	-	`sha256:ea75614c2ac46a6f8b4ec8e5590084bd62a808395e06766a98c7677f9be07e4b`  
		Last Modified: Wed, 09 Dec 2020 19:32:24 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26ca920a73d409b4bca897c5ace399567d216e9618bc7574b860e2d5ebe2c1c`  
		Last Modified: Wed, 09 Dec 2020 19:32:25 GMT  
		Size: 288.7 KB (288696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378a8c8912c1c6eb6efd36640da3abb567d310ef1a1fe73a4894f84d6dcb0340`  
		Last Modified: Mon, 14 Dec 2020 21:35:23 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5fd85c475fd2f7390849ac88e7b402871387048a5e1b0b04d81d465e5f06206`  
		Last Modified: Mon, 14 Dec 2020 21:35:23 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cfef50b4a087fa0f11400fe1d2af6e1caf8c1977ae65a3d40b5c852c2767d0`  
		Last Modified: Mon, 14 Dec 2020 21:35:23 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d74d4b2c649bcb9f9b61d9f5ffdc0a18f5e529f9ed006a2c51d775a5866481e`  
		Last Modified: Mon, 14 Dec 2020 21:38:44 GMT  
		Size: 184.9 MB (184852197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be34106cb3323915117c35fd60c7a0d791469decd551ab9e4a826ac9465b0475`  
		Last Modified: Mon, 14 Dec 2020 21:35:23 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-jdk` - windows version 10.0.14393.4104; amd64

```console
$ docker pull openjdk@sha256:037e3b00b9d7da95a072edee6778f9ac6323c9724d7b2bfd99fa721d9e08b147
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5974516802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a38d05e1eff361b7e737e6cdc2fbd08bffd38e90b797249589ce6a0434c43f`
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
# Wed, 09 Dec 2020 18:53:58 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 09 Dec 2020 18:55:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Mon, 14 Dec 2020 21:26:39 GMT
ENV JAVA_VERSION=16-ea+28
# Mon, 14 Dec 2020 21:26:42 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/28/GPL/openjdk-16-ea+28_windows-x64_bin.zip
# Mon, 14 Dec 2020 21:26:45 GMT
ENV JAVA_SHA256=501d49c571b04ef0817887c975cc3a24ddd839acd752852e23312d0d8752e270
# Mon, 14 Dec 2020 21:29:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Dec 2020 21:29:08 GMT
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
	-	`sha256:7efcedd72d8736d58697ed7ddad4a707710a4b5db13e76e520e7b8d89f1c82a3`  
		Last Modified: Wed, 09 Dec 2020 19:33:14 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d811bec4145213374f3541dd1f3b4b1d442fb2aed336c617caf8d34c06dc8356`  
		Last Modified: Wed, 09 Dec 2020 19:33:18 GMT  
		Size: 5.5 MB (5488120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ab0f5d0f10744c100467da1a3aaf6c690e42c413165276864d073c67099e73`  
		Last Modified: Mon, 14 Dec 2020 21:39:12 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de8af8d6c1e9c0f595139e90c83cd4da9f164896674f949a287d86c5d2a77e8d`  
		Last Modified: Mon, 14 Dec 2020 21:39:11 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31021b6fed0bff3e30646c0cfc20c16c19c5fc9f150ba9a2fc9933dcb4aebae5`  
		Last Modified: Mon, 14 Dec 2020 21:39:11 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12474bada6b4b6d08fd36f0df06ba71f910a62096e2d8e45abc709aca747b37`  
		Last Modified: Mon, 14 Dec 2020 21:42:36 GMT  
		Size: 190.1 MB (190130999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5addea0299edb1b574ef0a74332b4e1bd538d9ab2a3916367a5cf15a3d9db783`  
		Last Modified: Mon, 14 Dec 2020 21:39:12 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
