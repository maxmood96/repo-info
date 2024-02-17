## `openjdk:23-ea-10-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e2ece059955d1b6402b0ecd451efd58cbe3797611d3b5ef882a1283b565aa7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `openjdk:23-ea-10-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull openjdk@sha256:9a7f8d6e28731a312d6f56d0c92dba45abdc5ff23b1c501e97d526f4cb1a3abd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2109440800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31155a4fe4280a6b26e7f1c937a222c7524a498f86032418ed5fe5c4338970f7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Sat, 17 Feb 2024 01:00:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 17 Feb 2024 01:00:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:00:51 GMT
ENV JAVA_HOME=C:\openjdk-23
# Sat, 17 Feb 2024 01:00:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:00:57 GMT
ENV JAVA_VERSION=23-ea+10
# Sat, 17 Feb 2024 01:00:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/10/GPL/openjdk-23-ea+10_windows-x64_bin.zip
# Sat, 17 Feb 2024 01:00:59 GMT
ENV JAVA_SHA256=c8a55ee2916486b9f5f0000b52d73eab80af9b18f48a74bf8269f14057b12371
# Sat, 17 Feb 2024 01:01:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 17 Feb 2024 01:01:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306d372aea48801a8b9c10373559b44856b63671216da01889c50ba4a2abd02e`  
		Last Modified: Sat, 17 Feb 2024 01:01:30 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a030a050ead85d6a2a51c8c7e3dcec45164ef9afdfde46b93791faf03aba4c`  
		Last Modified: Sat, 17 Feb 2024 01:01:30 GMT  
		Size: 504.9 KB (504901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45fe9156d517100348a9c6fab58a17da95c344dc9f1e365176557ab4abf49b10`  
		Last Modified: Sat, 17 Feb 2024 01:01:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2399928af94a8c69d27d8683f22167f5b012750e92083056fce8f1917e118139`  
		Last Modified: Sat, 17 Feb 2024 01:01:30 GMT  
		Size: 355.4 KB (355419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166a9a1ffdcf2bd4354884ac659649796c176590fcf6d14bdefce400a0c48b66`  
		Last Modified: Sat, 17 Feb 2024 01:01:28 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc6a4ffa071f66d606abc6744a819b520adc0650e58e7f56838a7ac71b16406b`  
		Last Modified: Sat, 17 Feb 2024 01:01:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4c4cc97faf1836f9ac60f4d7b7e643920b67bad93a25a621f0de3bbf6fe340`  
		Last Modified: Sat, 17 Feb 2024 01:01:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1c059eabb693611a93812031aff1eefc5ad119b2c75dec541a98b3cd52ee105`  
		Last Modified: Sat, 17 Feb 2024 01:01:40 GMT  
		Size: 197.9 MB (197918561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:042b49a47e9278832ea8348c5a1dc81e177a490bed58841dcbde9cfc45b215d5`  
		Last Modified: Sat, 17 Feb 2024 01:01:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
