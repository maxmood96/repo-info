## `openjdk:23-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9f31f3730d62ebfa39ebae97375b6597c40f655094b6fb97e5edb6e993fc5578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `openjdk:23-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull openjdk@sha256:ee2378888fd65cc1cb3ffaf41a923a5684f0f7d29e8538407223f8bc1107504b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2155864289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5e2ab62d0e85e3bad3fae5cd3a334781dceaec468f5151be3f82e15ab9fbecb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 25 Mar 2024 19:12:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 25 Mar 2024 19:12:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:12:55 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 25 Mar 2024 19:13:03 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:13:04 GMT
ENV JAVA_VERSION=23-ea+15
# Mon, 25 Mar 2024 19:13:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/15/GPL/openjdk-23-ea+15_windows-x64_bin.zip
# Mon, 25 Mar 2024 19:13:05 GMT
ENV JAVA_SHA256=990a13730f096e195392211ecd4623c364cae742a9aedb5aae232c629b08f2b6
# Mon, 25 Mar 2024 19:13:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 25 Mar 2024 19:13:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f8557839336a7916e35f38d2bc8ffa6f5cae2c4078eec439dd2ed236bb0264`  
		Last Modified: Mon, 25 Mar 2024 19:13:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9caf8f1404b63352316c4b57850e0419f245ba118fb9c45202072a58f231a6e5`  
		Last Modified: Mon, 25 Mar 2024 19:13:40 GMT  
		Size: 505.0 KB (504962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2162f9d2c138b0479b408efb83767e6c9b42978841d50770732475fa18ab71`  
		Last Modified: Mon, 25 Mar 2024 19:13:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a4d6ba2765f04bbfa84a9778c0395a659260edb41ce7775750855a42d6cf61`  
		Last Modified: Mon, 25 Mar 2024 19:13:39 GMT  
		Size: 345.4 KB (345444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e46e9e8b6fb401af7fe860134cc17df22b08b6da94a6541fc0cbe315de08c1`  
		Last Modified: Mon, 25 Mar 2024 19:13:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ca1a63bc2d0b667b9f352812c41bff32a05ab075d43c91315bc8904500f1d2`  
		Last Modified: Mon, 25 Mar 2024 19:13:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c3839c5da6424358591d4dce122b39af2a923a548932f39c866f0b7417d6d0`  
		Last Modified: Mon, 25 Mar 2024 19:13:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8015ac97f73ef57e49b6ddd8db49af70f0d5053243f067e7fd14499c9fbadf`  
		Last Modified: Mon, 25 Mar 2024 19:13:48 GMT  
		Size: 197.5 MB (197547154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:707ba728e6851bd46be3d420e92e7d295d6601e8db8f27adae72ec98906ee348`  
		Last Modified: Mon, 25 Mar 2024 19:13:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
