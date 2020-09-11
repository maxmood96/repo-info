## `openjdk:16-ea-jdk`

```console
$ docker pull openjdk@sha256:6b87ebaca93f459412a5be0e82db6c26ac3dd707c16ab9a4da3a336cf66fed4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.1457; amd64
	-	windows version 10.0.14393.3930; amd64

### `openjdk:16-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:39f2a35016dc3ec59ecd64ac7baca39a229e55a5aa6a30fd514937b01aa3f9dd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.3 MB (263293561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa65421ccda1c24629d00dd68509d97bdb8567c2fb1ec62402dd0f1ff1ad62f4`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 30 Aug 2018 21:49:27 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 24 Jul 2020 00:21:31 GMT
ADD file:02670bc2999f43239e261c6f4e819f10471cfababa139f0eeba033a934c44eed in / 
# Fri, 24 Jul 2020 00:21:31 GMT
CMD ["/bin/bash"]
# Wed, 26 Aug 2020 21:28:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 01 Sep 2020 01:41:13 GMT
ENV LANG=C.UTF-8
# Tue, 01 Sep 2020 01:41:13 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Tue, 01 Sep 2020 01:41:13 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Sep 2020 20:18:46 GMT
ENV JAVA_VERSION=16-ea+14
# Tue, 08 Sep 2020 20:19:30 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/14/GPL/openjdk-16-ea+14_linux-aarch64_bin.tar.gz; 			downloadSha256=4924fb671a224f19c55fb3e74e3ed7bea9b32e76545671803204997e8b7b24bf; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/14/GPL/openjdk-16-ea+14_linux-x64_bin.tar.gz; 			downloadSha256=c5006de0056bf35a4fafcf28c24f5a9a96078c704b074cdb58b00dec463b1488; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Sep 2020 20:19:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1bbe67b820dbc81dda19341c188f2504cb57d03d540dc94bf12e3f752102adf8`  
		Last Modified: Fri, 24 Jul 2020 00:23:22 GMT  
		Size: 53.2 MB (53238241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c479ccfad94616e2be168f7843f91429bd9a7d0996b687d670bfe633136895a`  
		Last Modified: Wed, 26 Aug 2020 21:33:04 GMT  
		Size: 13.4 MB (13417665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c3a6eef2d92fae3471797a85b6a1b402ca7a5a0f2bfb7608515ae583dd5cd4`  
		Last Modified: Tue, 08 Sep 2020 20:24:12 GMT  
		Size: 196.6 MB (196637655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b86c955f43383215c18f7ab15b9d08db05f687cdebb96c89ac9a3f2a430c490b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.8 MB (242821860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:052859d6e5ac41020737758794d229fc994b89652cc2c0afaae8587a1574c12d`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 31 May 2019 21:40:52 GMT
MAINTAINER Oracle Linux Product Team <ol-ovm-info_ww@oracle.com>
# Fri, 11 Sep 2020 06:39:42 GMT
ADD file:c8745918ce90d90daefed5ea00db8b400158109f53a85988975f96ce7084c609 in / 
# Fri, 11 Sep 2020 06:39:46 GMT
CMD ["/bin/bash"]
# Fri, 11 Sep 2020 07:09:36 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Fri, 11 Sep 2020 07:09:38 GMT
ENV LANG=C.UTF-8
# Fri, 11 Sep 2020 07:09:38 GMT
ENV JAVA_HOME=/usr/java/openjdk-16
# Fri, 11 Sep 2020 07:09:39 GMT
ENV PATH=/usr/java/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Sep 2020 07:09:40 GMT
ENV JAVA_VERSION=16-ea+14
# Fri, 11 Sep 2020 07:10:14 GMT
RUN set -eux; 		objdump="$(command -v objdump)"; 	arch="$(objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		arm64 | aarch64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/14/GPL/openjdk-16-ea+14_linux-aarch64_bin.tar.gz; 			downloadSha256=4924fb671a224f19c55fb3e74e3ed7bea9b32e76545671803204997e8b7b24bf; 			;; 		amd64 | i386:x86-64) 			downloadUrl=https://download.java.net/java/early_access/jdk16/14/GPL/openjdk-16-ea+14_linux-x64_bin.tar.gz; 			downloadSha256=c5006de0056bf35a4fafcf28c24f5a9a96078c704b074cdb58b00dec463b1488; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Sep 2020 07:10:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b0a89fc27ec40345cd34fac22c2caa5adb9d10c730a6bd900435007be8e8ac80`  
		Last Modified: Fri, 11 Sep 2020 06:41:50 GMT  
		Size: 53.3 MB (53291835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54565c8f5569913127216a9630522b7177b23429e528cdd38041680808117936`  
		Last Modified: Fri, 11 Sep 2020 07:13:47 GMT  
		Size: 14.3 MB (14311816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3137ed5f564ea8d0223838f480500eaf60d126cd66e6a85666a026ca271cae42`  
		Last Modified: Fri, 11 Sep 2020 07:14:12 GMT  
		Size: 175.2 MB (175218209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-jdk` - windows version 10.0.17763.1457; amd64

```console
$ docker pull openjdk@sha256:1e44ef6aa7f350e5a5130871213ae7cacd568f222a832f1d419f8dd7d061feb1
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2557597344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5915fa36def6c5dead5b73c36b0c3c4436482fa9ac4faa785db3ecd590e1e5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Tue, 08 Sep 2020 19:36:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Sep 2020 20:05:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 08 Sep 2020 20:05:14 GMT
ENV JAVA_HOME=C:\openjdk-16
# Tue, 08 Sep 2020 20:05:42 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 08 Sep 2020 20:05:43 GMT
ENV JAVA_VERSION=16-ea+14
# Tue, 08 Sep 2020 20:05:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/14/GPL/openjdk-16-ea+14_windows-x64_bin.zip
# Tue, 08 Sep 2020 20:05:45 GMT
ENV JAVA_SHA256=1b6ed89998fe831c6d9abb5d610675427775247f839acd698d367954ee8d4fdb
# Tue, 08 Sep 2020 20:07:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Sep 2020 20:07:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5af76ffebd6bf4f1b787b4a988842077427c65d101c4e4c449f02b8cea0332cd`  
		Last Modified: Tue, 08 Sep 2020 19:54:19 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b301c9d4a0d508778c4b1506920d1304eb5d8c3d5a73ee0a1b522db1e8b9d70`  
		Last Modified: Tue, 08 Sep 2020 22:27:29 GMT  
		Size: 9.1 MB (9130218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b7534d2f9d4d5435b384e825c98f305b60fa3ec2ddb9c869a6b6fcdec1d25`  
		Last Modified: Tue, 08 Sep 2020 22:27:26 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfb7f69d9fbf5629248814c6623d7a21a84cfe9a45d7b548045b31caa10fd0d`  
		Last Modified: Tue, 08 Sep 2020 22:27:26 GMT  
		Size: 295.1 KB (295145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:672ddc46b4936e3fcb143ee14d72a93353c6ec7cb9022d07040ece55667acb71`  
		Last Modified: Tue, 08 Sep 2020 22:27:23 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59508f647eec88811bc7a3680ac30fe5db90cb53d6d0fe6770c69bd1283ca6c`  
		Last Modified: Tue, 08 Sep 2020 22:27:23 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:064635d6c4d5e48b4611650c4488cc7338a0b21d41198534cb7fd2ea91e4ea05`  
		Last Modified: Tue, 08 Sep 2020 22:27:23 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3c8816eba81d4725d7a207492386f3fdc97a939cceb61b524b41d6a09b57c93`  
		Last Modified: Tue, 08 Sep 2020 22:27:46 GMT  
		Size: 196.9 MB (196892954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae1e11a8e91370bcb2180df61335da5a4912924bd5308be2163accf187c1ab7`  
		Last Modified: Tue, 08 Sep 2020 22:27:23 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:16-ea-jdk` - windows version 10.0.14393.3930; amd64

```console
$ docker pull openjdk@sha256:39299460a98028907da1ded3d95173ce0455673a1b16e88664b4be3aa5dcd70a
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5956544945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a382868dc000aca8822952dd61bd6fd60423bea5da87ebeac73f8bbec93afd47`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 08 Sep 2020 19:31:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Sep 2020 20:09:21 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 08 Sep 2020 20:09:22 GMT
ENV JAVA_HOME=C:\openjdk-16
# Tue, 08 Sep 2020 20:10:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Tue, 08 Sep 2020 20:10:44 GMT
ENV JAVA_VERSION=16-ea+14
# Tue, 08 Sep 2020 20:10:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/14/GPL/openjdk-16-ea+14_windows-x64_bin.zip
# Tue, 08 Sep 2020 20:10:45 GMT
ENV JAVA_SHA256=1b6ed89998fe831c6d9abb5d610675427775247f839acd698d367954ee8d4fdb
# Tue, 08 Sep 2020 20:13:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Sep 2020 20:13:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8f6f82df7cca9113965bd35d2921a651250266aa7a3a9df6a0a42e8c005f1333`  
		Last Modified: Tue, 08 Sep 2020 19:53:55 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbeff382f1371b6819ca1ae810348afda32084cbd4526c4114c9ff5f85a5d6d`  
		Last Modified: Tue, 08 Sep 2020 22:28:21 GMT  
		Size: 9.9 MB (9886373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7ce5a5f1c846bc13c012040ba007559f48bfa1c47939f5ef2dd12a157bf9e45`  
		Last Modified: Tue, 08 Sep 2020 22:28:16 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7769f3897b358df537321f97bab12aff9a86e616ddaa588c3b91db0d0b65c1`  
		Last Modified: Tue, 08 Sep 2020 22:28:17 GMT  
		Size: 5.3 MB (5336442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44503f4a45f1d6b463b61a8471b323e93ca7e09452f87e2070c8114d68b713c5`  
		Last Modified: Tue, 08 Sep 2020 22:28:13 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fcd635d0dd2966b8cd7b3ecdb0b6064cbc17ebb69ce36d6f778de42c90dd57a`  
		Last Modified: Tue, 08 Sep 2020 22:28:13 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679242c149aacbb3c0922802b29a8248b53a53e6402b0740c98b51c99f0a252e`  
		Last Modified: Tue, 08 Sep 2020 22:28:12 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba1d009d40c39e81f1ae715f014151dd5067e6e6e7126a405b1dc78d6df255fe`  
		Last Modified: Tue, 08 Sep 2020 22:28:35 GMT  
		Size: 202.1 MB (202060841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707f18a9be56bc6ef5a9af7ea41c3a05628bf8b209605a09ddf761c26ec5e4d1`  
		Last Modified: Tue, 08 Sep 2020 22:28:13 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
