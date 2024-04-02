## `openjdk:23-ea-16-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:c716b5fbdaf9e0768c1b413acdc889031544cfa126671166c8ecc6b95ed471c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `openjdk:23-ea-16-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull openjdk@sha256:5d6fbd970dc5523bc27b918939468f12658d1deae6fb775f6cc69adaca8fb19a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2163967307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f79235e5256d1eae3dedbcfee3268c1d2eefbfb6b797474e5a550d90af35998`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 01 Apr 2024 23:49:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Apr 2024 23:50:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:50:09 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 01 Apr 2024 23:50:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:50:15 GMT
ENV JAVA_VERSION=23-ea+16
# Mon, 01 Apr 2024 23:50:16 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/16/GPL/openjdk-23-ea+16_windows-x64_bin.zip
# Mon, 01 Apr 2024 23:50:17 GMT
ENV JAVA_SHA256=d8f0d3c652a3ea74356d51353fc92684c73b07dba66500430adaec9353a30266
# Mon, 01 Apr 2024 23:50:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 01 Apr 2024 23:50:46 GMT
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
	-	`sha256:2503f7ecc2b5456184710df9a0479e9cea0e911963195b39d2026d28ccfa1810`  
		Last Modified: Mon, 01 Apr 2024 23:50:53 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59841f58cdc97ac6439ba48596ec97290c188d22991a04dd127fcd3999b1c87b`  
		Last Modified: Mon, 01 Apr 2024 23:50:53 GMT  
		Size: 499.2 KB (499229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09536f55b7bdcb7bdf02b283349038213e4495b19097b6feff8523ff464f317a`  
		Last Modified: Mon, 01 Apr 2024 23:50:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b99348680dcd2bfa3838ed265eb00bfb5a5d6b6190609c8549e95dfbda9f01c`  
		Last Modified: Mon, 01 Apr 2024 23:50:53 GMT  
		Size: 347.0 KB (346983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15b657b4c400b15e277baa77510c6f1afecd331b5a0ccf3242c23162c1931a8`  
		Last Modified: Mon, 01 Apr 2024 23:50:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8099defedec4760cb0848b6f487de60ef58944028804c0d0dc3e1cd11d367c07`  
		Last Modified: Mon, 01 Apr 2024 23:50:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f8fc14c4061d90e5a0161671195f4d10eae31f2383f23b7845acfe9010e6b4`  
		Last Modified: Mon, 01 Apr 2024 23:50:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cafc8fadd392d6a7ad5135999f440a56731b1b09ce09f6b4a649d6a197f991b8`  
		Last Modified: Mon, 01 Apr 2024 23:51:01 GMT  
		Size: 205.7 MB (205654334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88342fed94360e43d8cdfc6b6fb64b7c195eb067a3bdb355f480847a5617db95`  
		Last Modified: Mon, 01 Apr 2024 23:50:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
