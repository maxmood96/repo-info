## `openjdk:14-ea-34-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:e897516fcf96d3b13f4f59dd19242c742c703bd3ab25450603dce2b38021298b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64
	-	windows version 10.0.14393.3443; amd64

### `openjdk:14-ea-34-jdk-windowsservercore` - windows version 10.0.17763.973; amd64

```console
$ docker pull openjdk@sha256:2ca680fe12778d2ab721994f4896d12c444becd6135a4fad83f892a9c9a99254
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2416550190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad0034748b211a21fa61424d66f50591a3ea201a55da1d8bd7f809ab6ad6a8d7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2020 23:47:06 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Tue, 14 Jan 2020 23:58:14 GMT
ENV JAVA_HOME=C:\openjdk-14
# Tue, 14 Jan 2020 23:58:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 31 Jan 2020 17:55:10 GMT
ENV JAVA_VERSION=14-ea+34
# Fri, 31 Jan 2020 17:55:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/34/GPL/openjdk-14-ea+34_windows-x64_bin.zip
# Fri, 31 Jan 2020 17:55:13 GMT
ENV JAVA_SHA256=f0d3b92f45572c98f8855e51fe878817a603d1d3d9a160aec0af2c48bb589429
# Fri, 31 Jan 2020 17:57:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2020 17:57:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe8a4080f0d1077681de059bc8597064c929d967b370eac061cacf38283adfe`  
		Last Modified: Wed, 15 Jan 2020 01:45:23 GMT  
		Size: 4.5 MB (4547614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a55aa49d97e830f6b3c864cafda1aceff84ee42dab37ddded91a28efb13412be`  
		Last Modified: Wed, 15 Jan 2020 01:55:29 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa48874f549ecadb376734cb21f5139d255704082fc0a269d8667613fa7013c8`  
		Last Modified: Wed, 15 Jan 2020 01:55:29 GMT  
		Size: 289.5 KB (289491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3543dbeb90a5e2a4dc3c027166503b782ea86749d084fa38bdd6f046c2167b52`  
		Last Modified: Fri, 31 Jan 2020 18:10:15 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e3e7a53b1efb1a01b48795139aff1995a5f4ed0721cfed0c4209ea231489b9`  
		Last Modified: Fri, 31 Jan 2020 18:10:15 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b750959b39f6d14624ced6931520a29b2969b11107d0bd12ce87941a1731f0e6`  
		Last Modified: Fri, 31 Jan 2020 18:10:15 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42b9d76d4924cc3fce308cd9ad489825ac2612586ca37d754098f59bbf6a4131`  
		Last Modified: Fri, 31 Jan 2020 18:10:37 GMT  
		Size: 194.3 MB (194294696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f605d46f8801599823fc377a583f431a34074df9a5aa59a6bfb4f059058966`  
		Last Modified: Fri, 31 Jan 2020 18:10:15 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:14-ea-34-jdk-windowsservercore` - windows version 10.0.14393.3443; amd64

```console
$ docker pull openjdk@sha256:a5219d68dcb7ba62cb71ac97fd818baf1ace5ab5d725a9812e291dbf75ffca49
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5934689496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ad998acab3d9ab01f6304cba0842e646ec57f1c59ce3a3048bf866c692d351`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2020 23:51:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 15 Jan 2020 00:01:19 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 15 Jan 2020 00:02:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Fri, 31 Jan 2020 17:57:44 GMT
ENV JAVA_VERSION=14-ea+34
# Fri, 31 Jan 2020 17:57:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk14/34/GPL/openjdk-14-ea+34_windows-x64_bin.zip
# Fri, 31 Jan 2020 17:57:47 GMT
ENV JAVA_SHA256=f0d3b92f45572c98f8855e51fe878817a603d1d3d9a160aec0af2c48bb589429
# Fri, 31 Jan 2020 18:00:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 31 Jan 2020 18:00:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59f69707d10b5be4e5c56881ea890fd476325bea3b16b5a7e7c56a1d8b3f056`  
		Last Modified: Wed, 15 Jan 2020 01:46:54 GMT  
		Size: 5.4 MB (5386027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e40fa392055162d8b62010b964933f208b474a495503491293e2990c429114a1`  
		Last Modified: Wed, 15 Jan 2020 01:56:53 GMT  
		Size: 1.2 KB (1194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa76c12f7c4dc8568e6a71fb5adf4fd6a8c29f7eeb6d4ffe9c361967e5eb82d`  
		Last Modified: Wed, 15 Jan 2020 01:56:56 GMT  
		Size: 5.4 MB (5368309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a267518dcdd46d70307245a903457cd8d32aa47f9ad6ea0ea6f945025f47a7d8`  
		Last Modified: Fri, 31 Jan 2020 18:11:36 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cb12b6d509e584379b46b90eedae736292e0a327d8b08eeb1ee1f86122e772e`  
		Last Modified: Fri, 31 Jan 2020 18:11:36 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7f14e1a9a7dc51768d9f8453c9ecee5d2574b9a38af39489c00ebe4f8a7312`  
		Last Modified: Fri, 31 Jan 2020 18:11:36 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99b2f360c344464954bfd6736708d3dfb16b04f2fc84e13c3ac0bb4aa88c20a`  
		Last Modified: Fri, 31 Jan 2020 18:12:40 GMT  
		Size: 199.3 MB (199328801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b9d10138aa5f01b5fdd3012d7554e58a0cc3a9ac9f6e37d98d42962b3f8717`  
		Last Modified: Fri, 31 Jan 2020 18:11:36 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
