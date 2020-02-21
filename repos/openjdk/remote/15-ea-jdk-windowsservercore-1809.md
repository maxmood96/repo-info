## `openjdk:15-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:ed244b9336290ff7f5476b7c23c50fb45221261ba8c726bc5093d9fd1bf2abed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `openjdk:15-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull openjdk@sha256:71061bacbd9fdf31706c8db34d1bf51d81439d341cb66cf2504aafdd188c774d
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2428786364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:172b88d6e9687789239a4e128624555b3d20dce2b54a326b105392972042381a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 20 Feb 2020 01:14:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Thu, 20 Feb 2020 01:14:34 GMT
ENV JAVA_HOME=C:\openjdk-15
# Thu, 20 Feb 2020 01:15:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 21 Feb 2020 00:23:26 GMT
ENV JAVA_VERSION=15-ea+11
# Fri, 21 Feb 2020 00:23:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/11/GPL/openjdk-15-ea+11_windows-x64_bin.zip
# Fri, 21 Feb 2020 00:23:28 GMT
ENV JAVA_SHA256=1abf19d39af7342aca71521dd5b3bd98d6782fc727f44bdc36f8f390ba528bdb
# Fri, 21 Feb 2020 00:25:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 21 Feb 2020 00:25:42 GMT
CMD ["jshell"]
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
	-	`sha256:20f0782e4992ed8796b0b5659aad759ed2fb47d4fafaaa5a38afe4f993f94d68`  
		Last Modified: Thu, 20 Feb 2020 03:03:23 GMT  
		Size: 4.6 MB (4567940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b83b3b5abce3322c8ff4f4b887b48ae519c81efaf348894c9a75224c981e37`  
		Last Modified: Thu, 20 Feb 2020 03:03:20 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211d20742c6d6be7334058298e82bd2e728c2b30ec35eccc457a3a8283457c3e`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 291.1 KB (291148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce98dd0ac51f84830cd32dc8cdfdd1e9ef24acb89a4e042fc015aaf9640952c`  
		Last Modified: Fri, 21 Feb 2020 00:34:54 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b873b2d7660d275b2b45558757137d78d8ff8e11081691c7152b9f7fdf1fb85`  
		Last Modified: Fri, 21 Feb 2020 00:34:54 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a9fcf1cea0b8b7f5d882da1f59eba314c49480c51089b4d515b9d8032a09e5`  
		Last Modified: Fri, 21 Feb 2020 00:34:54 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6af0651823c8e715aa4f1a61cd40cadcf7a85e6f8031dcb7cba040755a7af7e`  
		Last Modified: Fri, 21 Feb 2020 00:35:17 GMT  
		Size: 193.4 MB (193416241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14c4f851c53326412d50cc22008ad94dd8126c1c7fd5c6a6f694a35dc96a558a`  
		Last Modified: Fri, 21 Feb 2020 00:34:54 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
