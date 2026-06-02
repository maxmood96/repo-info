## `openjdk:27-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:28798a8e0f80538b0753b50c09cb94fb909a28f16393e776f05c428a4a0bdd73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:2f1701bcc79424047629f4ec9a6417c7ab4b5c2b4c8316af5925973871872662
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2430281692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f454997fd298e5e5a63354fc03c8d528fa60378135b4d6f539d65c4fbce0ca4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 07:22:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 07:23:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:23:14 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 02 Jun 2026 07:23:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:23:20 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:23:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_windows-x64_bin.zip
# Tue, 02 Jun 2026 07:23:21 GMT
ENV JAVA_SHA256=5bbf96e8f91e2c80680961ba7cc2ddb7112131f6fa000d2472ab2ea6c99a06f7
# Tue, 02 Jun 2026 07:24:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:24:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b36a0f7c1b88527f3122c1904a3c2a5f59424c7fff771e9086acb32e1f45c706`  
		Last Modified: Tue, 02 Jun 2026 07:24:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac7bf73508dc8505e08d79e84e50a0e20c6ba5b0444e6ee24d6fda8358a2db3c`  
		Last Modified: Tue, 02 Jun 2026 07:24:23 GMT  
		Size: 430.1 KB (430085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083a7a1446cf1e262ac433bde4d61ed419fab06c207745312b2d9cabb3557313`  
		Last Modified: Tue, 02 Jun 2026 07:24:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b506c11d9bbe76029855d3759070d90cae2065f105a5a70554d37d06965d063e`  
		Last Modified: Tue, 02 Jun 2026 07:24:23 GMT  
		Size: 414.2 KB (414188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae9fd377d3ee337b1acbfb3d47d92c26d57168f76083ea9fc96b63f10427aa1`  
		Last Modified: Tue, 02 Jun 2026 07:24:21 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deaa3ea876cb84ffcdb0d4b2bec65e170299dc034a331db1bfa3d87e66c375b`  
		Last Modified: Tue, 02 Jun 2026 07:24:21 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780c0b3ce0b5af025bb7ace9038dc27ee3922bd9af8d76ce3311068234851b57`  
		Last Modified: Tue, 02 Jun 2026 07:24:21 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec94b2e848c8216c8737d5fc0a7626f677e6df81cfed21473455115aaa602da`  
		Last Modified: Tue, 02 Jun 2026 07:24:35 GMT  
		Size: 223.5 MB (223487891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c08dfeb7e4765495402b9234af1776fe9dac304835494bf9695b553908744e`  
		Last Modified: Tue, 02 Jun 2026 07:24:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
