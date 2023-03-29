## `openjdk:21-ea-jdk`

```console
$ docker pull openjdk@sha256:fd40e8c2a37ab5269e5e09394c917dec0c6e6e904b4559a378df1d677159bfd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1607; amd64
	-	windows version 10.0.17763.4131; amd64

### `openjdk:21-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:1e765dd1a8f6fa157fa6d33f42f7e2afd816a907f517fb90211775966d05328c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.1 MB (261139952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c451870e361cf7f6dc5c0c57a64b1acb82c67c89864da9030edd65bca9c266a`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Mar 2023 00:21:35 GMT
ADD file:728bdb9bb48c571a53579f02c3df258a071a1612cb28160c8348fd0b83893f1a in / 
# Wed, 29 Mar 2023 00:21:35 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:39:18 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:39:18 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 29 Mar 2023 00:39:18 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 00:39:18 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 00:39:18 GMT
ENV JAVA_VERSION=21-ea+15
# Wed, 29 Mar 2023 00:39:28 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='0fec1002b8c8975b181bd6966a817028d6b373cbc759254231f9b96db1fe6edd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93cc1eb6202093a127f1f9ed2e866a51dff29321f878085c18f317cefb113ffc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Mar 2023 00:39:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d98f7984035168bbebf20a188b8cf4aa680c740ceff10816dcbbd32a58483843`  
		Last Modified: Wed, 29 Mar 2023 00:23:00 GMT  
		Size: 44.6 MB (44562176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76522ebbbebe1d33d391848d9f7910bda3808bb7ca0ec5f2a7f84db25521768`  
		Last Modified: Wed, 29 Mar 2023 00:40:36 GMT  
		Size: 15.0 MB (15006652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e21df7acaee6af113a84facd0a98a4333a3b99a721e8a086a1d8ec388cf026c`  
		Last Modified: Wed, 29 Mar 2023 00:40:48 GMT  
		Size: 201.6 MB (201571124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:b63242539e333f181a05f7d40f16ae18da4cc71d8aa4a309e806c5562330ea5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.4 MB (259356063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6073ac1fc33d44fe0bb06ed99a4173f83bb2d54449dedbb7d2d26e08c11d3fb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 29 Mar 2023 00:40:08 GMT
ADD file:9a1aa8ba1b4f81ac1090ea3164805b0e7f754f52551d359e5e78519b09b17406 in / 
# Wed, 29 Mar 2023 00:40:08 GMT
CMD ["/bin/bash"]
# Wed, 29 Mar 2023 00:59:46 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 29 Mar 2023 00:59:46 GMT
ENV JAVA_HOME=/usr/java/openjdk-21
# Wed, 29 Mar 2023 00:59:46 GMT
ENV PATH=/usr/java/openjdk-21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Mar 2023 00:59:46 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 00:59:46 GMT
ENV JAVA_VERSION=21-ea+15
# Wed, 29 Mar 2023 00:59:55 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-x64_bin.tar.gz'; 			downloadSha256='0fec1002b8c8975b181bd6966a817028d6b373cbc759254231f9b96db1fe6edd'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_linux-aarch64_bin.tar.gz'; 			downloadSha256='93cc1eb6202093a127f1f9ed2e866a51dff29321f878085c18f317cefb113ffc'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 29 Mar 2023 00:59:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:dd2958b1d3c5393ad5809ad7b967b3cec62361b73fa73f90b67cc29eaf2308b0`  
		Last Modified: Wed, 29 Mar 2023 00:41:25 GMT  
		Size: 43.5 MB (43476988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015334e79538f75edd26ca4da7bffb8eb69d94d9292d602053b1fd07f37c8cee`  
		Last Modified: Wed, 29 Mar 2023 01:01:08 GMT  
		Size: 15.8 MB (15844650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34f8291c956e0648177e2c357ab96eda4c15cc9c5eca0d7f80a495e120a34ba`  
		Last Modified: Wed, 29 Mar 2023 01:01:18 GMT  
		Size: 200.0 MB (200034425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk` - windows version 10.0.20348.1607; amd64

```console
$ docker pull openjdk@sha256:812075e8edfded5239819c5dd823e309f0a71ff56f81aa3ae2da78bf71958432
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1911945035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9aa862ae1caca213115fe68d05069c57ee2b7e0e6860ed705c093333c9f9391`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 00:38:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 04:14:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Mar 2023 04:14:26 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Mar 2023 04:14:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Mar 2023 22:22:14 GMT
ENV JAVA_VERSION=21-ea+15
# Mon, 27 Mar 2023 22:22:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_windows-x64_bin.zip
# Mon, 27 Mar 2023 22:22:16 GMT
ENV JAVA_SHA256=194a0a04791fc11ea7622eb63e52f09091e9036c634e905b5394dbbf5a894533
# Mon, 27 Mar 2023 22:23:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Mar 2023 22:23:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bca4593035ae0e8d1b6e6eb1b053fddc6a6824b28f45f99de726d752d2c0f72`  
		Last Modified: Thu, 16 Mar 2023 01:39:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9232261c30bc22ec57212f386e8fea077a0775299f58234bfec01a611d98144`  
		Last Modified: Thu, 16 Mar 2023 04:30:43 GMT  
		Size: 736.0 KB (736009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545d4a9e39b1cc7dac0d42fb0a331c120f1bfed624e7850e1faa4eb99110ce01`  
		Last Modified: Thu, 16 Mar 2023 04:30:43 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8063d1ae112267a681a9e7feb4d398e107825072b3fd2b95b3bad2efc8571978`  
		Last Modified: Thu, 16 Mar 2023 04:30:43 GMT  
		Size: 538.0 KB (538004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ada6097a0712a1b64919af01be3f78116d148aa1e9e4ca58f25b83fdd9b6d51f`  
		Last Modified: Mon, 27 Mar 2023 22:27:38 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031650a3ce38d903549f748280f1fd177b7d19a823233164fab304b9ccb39d02`  
		Last Modified: Mon, 27 Mar 2023 22:27:38 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da5545be8b4e5bbcbddac91cf712170b6d0de3229c6646044328839b4dffbae`  
		Last Modified: Mon, 27 Mar 2023 22:27:38 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8681c915a29ca129e86f3019502327d07af8babd1a40cb8e518f62d01a944a1`  
		Last Modified: Mon, 27 Mar 2023 22:27:59 GMT  
		Size: 196.7 MB (196722512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6f76e9798b9751fc4c45bba8f65835d76b1753d69dd0128272b03b4808d4b6`  
		Last Modified: Mon, 27 Mar 2023 22:27:38 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:21-ea-jdk` - windows version 10.0.17763.4131; amd64

```console
$ docker pull openjdk@sha256:66d48240566bdb8b80fe201e3a3527bed8fe4e9fa3da4c90f38bb223fde43946
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2210814807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87854becc369555eb92a8f962ace3eea1625697d0ca584014b36126d1f961136`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Sat, 11 Mar 2023 10:37:22 GMT
RUN Install update 10.0.17763.4131
# Thu, 16 Mar 2023 00:41:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 16 Mar 2023 04:17:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 16 Mar 2023 04:17:50 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Mar 2023 04:19:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 27 Mar 2023 22:23:43 GMT
ENV JAVA_VERSION=21-ea+15
# Mon, 27 Mar 2023 22:23:44 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/15/GPL/openjdk-21-ea+15_windows-x64_bin.zip
# Mon, 27 Mar 2023 22:23:45 GMT
ENV JAVA_SHA256=194a0a04791fc11ea7622eb63e52f09091e9036c634e905b5394dbbf5a894533
# Mon, 27 Mar 2023 22:25:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 27 Mar 2023 22:25:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a92048040b3b13af10f8287baabaddbb2759dfc77b1fb43f89b38b3275467f93`  
		Last Modified: Thu, 16 Mar 2023 01:42:29 GMT  
		Size: 305.6 MB (305565048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8e4e0836091bdd33e8adb56d1e13b8096550727a20534e2a2ab9298c86fa09`  
		Last Modified: Thu, 16 Mar 2023 01:41:16 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6954ad7da48d4dd7acf8132bc41996dfcd7f157b30b2ca35ec4814ffc26a94d3`  
		Last Modified: Thu, 16 Mar 2023 04:31:25 GMT  
		Size: 480.4 KB (480436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8087e24b23846aed99e303ff6d5268f444daecd74c150fb70198dabc16487141`  
		Last Modified: Thu, 16 Mar 2023 04:31:25 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2836db1b10d5ae1b6c026b5fc8f9667c86fafa8854926472e99f786aea1aaf7f`  
		Last Modified: Thu, 16 Mar 2023 04:31:25 GMT  
		Size: 309.7 KB (309740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2eb1ec860aef35e675342bf321b439345a6037097c8f29381ee88b3cd3f4591`  
		Last Modified: Mon, 27 Mar 2023 22:28:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0845d906ad6f034b0679a73365138b67743ade1fd239b4074ac9402b1fc01af9`  
		Last Modified: Mon, 27 Mar 2023 22:28:32 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5233d5117ca06476e2294658cff359fce5840f62b54c8704367fa3d6d2da8f0c`  
		Last Modified: Mon, 27 Mar 2023 22:28:33 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c306f88fa21e58c501f958b9e05374a4579e31b661d0018db8b59be2de78b622`  
		Last Modified: Mon, 27 Mar 2023 22:28:53 GMT  
		Size: 196.5 MB (196507156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a733fa4ee18f074bd6f76442cb6f627d0e7056bdbdda6592f2c87df5214d4bf`  
		Last Modified: Mon, 27 Mar 2023 22:28:33 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
