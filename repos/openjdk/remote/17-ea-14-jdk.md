## `openjdk:17-ea-14-jdk`

```console
$ docker pull openjdk@sha256:ad471abf75b67e6a75c28501e3166873cbfef9e43a27e8f7224618365949d1fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1817; amd64
	-	windows version 10.0.14393.4283; amd64

### `openjdk:17-ea-14-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:16a54e7864c1e7432a9b0430a4098934a13525e4eb3dfc950dbd494764b2e576
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.9 MB (240927147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d006149fd0b3b0a95d03039344475bb668f25734f888a8ccd40191bd1c3354`
-	Default Command: `["jshell"]`

```dockerfile
# Tue, 09 Mar 2021 20:36:33 GMT
ADD file:2ba8f9c8e1d7e464c075fdd46e81f2e15a69d9a5aefb4b991cccb352e082af2f in / 
# Tue, 09 Mar 2021 20:36:33 GMT
CMD ["/bin/bash"]
# Tue, 09 Mar 2021 20:55:08 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 09 Mar 2021 20:55:08 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Tue, 09 Mar 2021 20:55:08 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Mar 2021 20:55:08 GMT
ENV LANG=C.UTF-8
# Fri, 19 Mar 2021 18:23:43 GMT
ENV JAVA_VERSION=17-ea+14
# Fri, 19 Mar 2021 18:24:20 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/14/GPL/openjdk-17-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='d4bfd596e0b4f3eefb416719a5b6ad98ab3f37f27855573e7c94526a4ffad7d2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/14/GPL/openjdk-17-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='16646d2498690f98b44f196e74da8361ef05155038a04cb6f62fbb76df08e72f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 Mar 2021 18:24:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:63e877180dd1388e46564a2b7a72ddf3559dc506f4b6e8b435ed569643811c02`  
		Last Modified: Mon, 01 Feb 2021 20:34:13 GMT  
		Size: 42.1 MB (42069114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9ff0a89ff9842ef20925cd26efa5ab427f6c745febbbe471cc0a48bcc14e60`  
		Last Modified: Tue, 09 Mar 2021 21:08:26 GMT  
		Size: 13.3 MB (13280925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2513892d70e98dca336e46efd2e8983f6896f449b58c3feefac09d4823880c`  
		Last Modified: Fri, 19 Mar 2021 18:29:49 GMT  
		Size: 185.6 MB (185577108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-14-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:e9757f40025a46275efe893149253f811d749b62d02c71afb5450c608d650f91
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.7 MB (237713529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70919cac7393c7de20c37aaab93636079e6165ca8a067287b201c154247bc71e`
-	Default Command: `["jshell"]`

```dockerfile
# Mon, 01 Feb 2021 21:00:54 GMT
ADD file:40a46ad11c4530459867a348c980e7ed1ba9fe6bdf74da38208ee8bf7be1f81d in / 
# Mon, 01 Feb 2021 21:00:56 GMT
CMD ["/bin/bash"]
# Mon, 01 Feb 2021 21:05:57 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Mon, 01 Feb 2021 21:05:58 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Mon, 01 Feb 2021 21:05:58 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 01 Feb 2021 21:05:59 GMT
ENV LANG=C.UTF-8
# Fri, 19 Mar 2021 19:00:09 GMT
ENV JAVA_VERSION=17-ea+14
# Fri, 19 Mar 2021 19:01:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/14/GPL/openjdk-17-ea+14_linux-x64_bin.tar.gz'; 			downloadSha256='d4bfd596e0b4f3eefb416719a5b6ad98ab3f37f27855573e7c94526a4ffad7d2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/14/GPL/openjdk-17-ea+14_linux-aarch64_bin.tar.gz'; 			downloadSha256='16646d2498690f98b44f196e74da8361ef05155038a04cb6f62fbb76df08e72f'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 19 Mar 2021 19:01:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:17e75779b55909cd6075d706cc3fc9f838f287de73b35be3d551231217cbd32c`  
		Last Modified: Mon, 01 Feb 2021 21:02:50 GMT  
		Size: 42.0 MB (41996203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25fad58a53edbb48f3027bc56f941db82a77fd6d28a6fc25d4bf2462f3bc62bc`  
		Last Modified: Mon, 01 Feb 2021 21:15:35 GMT  
		Size: 14.1 MB (14057108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6551a561eb6d83fc5941447fcada08d1616a484c6de44f202667f934c38643cf`  
		Last Modified: Fri, 19 Mar 2021 19:07:17 GMT  
		Size: 181.7 MB (181660218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-14-jdk` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:6bfe0dbbbe66b451efdba3b2b72f50374debdf2a1ffb9720f87bf649ff90ea57
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2656737897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98860d72e0448b28a083461dde2f42c5f55ab46888636635209a4c1397aa31e8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 17:43:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:43:18 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Mar 2021 17:43:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 19 Mar 2021 19:15:27 GMT
ENV JAVA_VERSION=17-ea+14
# Fri, 19 Mar 2021 19:15:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/14/GPL/openjdk-17-ea+14_windows-x64_bin.zip
# Fri, 19 Mar 2021 19:15:29 GMT
ENV JAVA_SHA256=bb67e52010e2fcab6f54a97cf4b9124b66ae27bb3f2edc17a77a0a681e6b166e
# Fri, 19 Mar 2021 19:16:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 19 Mar 2021 19:16:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5a565fbc6dee6b0e5a6252ca763370a8d3521925db3d451dd6e7ec0efc1b07`  
		Last Modified: Wed, 10 Mar 2021 18:28:58 GMT  
		Size: 9.5 MB (9457788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce65a7afaa8a843f59f4e00b2cde68e50c25b4931a7ce73ff3b55438bd7742bf`  
		Last Modified: Wed, 10 Mar 2021 18:28:54 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2620c5b70d10c22e375ff81365a7e5c381fd1cb523ae714bcb824d42a5a46c51`  
		Last Modified: Wed, 10 Mar 2021 18:28:55 GMT  
		Size: 334.1 KB (334116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02be5c23bd235d6f3e9560c98e9c473206f30a8291eedb2c4243917759008d80`  
		Last Modified: Fri, 19 Mar 2021 19:26:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5776f96dfb772a36e48d590af566ebc49854542a7581323712c2fc9bb49874c`  
		Last Modified: Fri, 19 Mar 2021 19:26:47 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e803b79b97660a318906df4dece9970eea604be8eae59811a92eda1b3c698d8`  
		Last Modified: Fri, 19 Mar 2021 19:26:47 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d455578ca38563e31b214ac87b4b665c216a507bc9986b6f2b91dd54f12d88aa`  
		Last Modified: Fri, 19 Mar 2021 19:27:08 GMT  
		Size: 185.4 MB (185403020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cb193f6e98740333137fd49752e8ea1ef9476f1dc4d499a1fd8fa154b69a7e`  
		Last Modified: Fri, 19 Mar 2021 19:26:47 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:17-ea-14-jdk` - windows version 10.0.14393.4283; amd64

```console
$ docker pull openjdk@sha256:f4c1ff0df5efff23d53f1eef20688356a1a5a6d1af5afb2fd171acfc1c8ef2b8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6003524239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:281b106f9504180a15fde1f733522aeef4feebf451def2f90866a737593a7a09`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Mar 2021 18:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Mar 2021 13:42:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 17:46:47 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:46:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Mar 2021 17:48:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 19 Mar 2021 19:16:56 GMT
ENV JAVA_VERSION=17-ea+14
# Fri, 19 Mar 2021 19:16:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/14/GPL/openjdk-17-ea+14_windows-x64_bin.zip
# Fri, 19 Mar 2021 19:16:58 GMT
ENV JAVA_SHA256=bb67e52010e2fcab6f54a97cf4b9124b66ae27bb3f2edc17a77a0a681e6b166e
# Fri, 19 Mar 2021 19:19:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 19 Mar 2021 19:19:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30bda99601c5cbd3b2118409f401852ea648e2319bd81518723e476b28d764c5`  
		Size: 1.7 GB (1726924885 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76680da9dc6db108ddf2e353c494b45e8486a6751619a13ed8fb3ad64b9a16e9`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acde2be15530c0b8fb3d57db65ee292b515e7911dbd4b55109e48dbd55c28539`  
		Last Modified: Wed, 10 Mar 2021 18:33:09 GMT  
		Size: 10.2 MB (10177023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8e176190222d82d02bad5231e85a830ea393cb1c2afab482c0ab55ba9bc304`  
		Last Modified: Wed, 10 Mar 2021 18:32:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349d082f4a3335d41d13ed8c56f2b3e9212291e7de2c29a3a7c2bf5d5ed2f7ab`  
		Last Modified: Wed, 10 Mar 2021 18:32:59 GMT  
		Size: 5.6 MB (5605916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06eb1383826631e1e9a5e382aa55c571c7483d0cad7a93cebf15cbbfb56d36c4`  
		Last Modified: Fri, 19 Mar 2021 19:27:32 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410a4e6c70547e57308dd3ff5894580a62eb9a144636546a12b856ffafcf0748`  
		Last Modified: Fri, 19 Mar 2021 19:27:32 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579644cf5ab2878e3f75607ac102af8fc3e6e143baa9d6c944c3da7740fb6c94`  
		Last Modified: Fri, 19 Mar 2021 19:27:33 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4c588626faace2f2dafd924ab62f82fa44d6a2dbbf0b952e5aef3ad3a00fe7`  
		Last Modified: Fri, 19 Mar 2021 19:27:54 GMT  
		Size: 190.8 MB (190822030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b197dd745c627c5807801f3fb1517e218580111eeace017ba5959f13cc146239`  
		Last Modified: Fri, 19 Mar 2021 19:27:32 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
