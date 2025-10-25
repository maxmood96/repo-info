## `openjdk:26-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:ad146e0c612922ac403637d99e2045542ac551b893203688db25672a0907f974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `openjdk:26-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull openjdk@sha256:3602f5056a2c70466ea172ed1ce32a8c6a8e491657bd2ad622ffebc2e2790e8d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3442611305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a47bd7bd8ff9209eaf8fb850eddf9a80077c0b4025d1ec0f5c238b0d0486120`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 23:19:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 23:20:03 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 23:20:03 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 24 Oct 2025 23:20:08 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 24 Oct 2025 23:20:08 GMT
ENV JAVA_VERSION=26-ea+21
# Fri, 24 Oct 2025 23:20:09 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/21/GPL/openjdk-26-ea+21_windows-x64_bin.zip
# Fri, 24 Oct 2025 23:20:10 GMT
ENV JAVA_SHA256=25b332cae815558e365575910625e421a10ecbf655f0ed2d480d42f3224e9b93
# Fri, 24 Oct 2025 23:20:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 23:20:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b5a539c3fb46c1feb7dcbd3271a21d40927b7f95c22190432e7f6726a6d74b`  
		Last Modified: Fri, 24 Oct 2025 23:28:58 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3502c94f74201aae42eaf45f2ba0e7a27da39e891f177f81389cd2a7a4ce535`  
		Last Modified: Fri, 24 Oct 2025 23:28:58 GMT  
		Size: 350.1 KB (350091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5c26881b8730b875ca21d7ba2a0f19e608546879d853cb7538bc02754356db`  
		Last Modified: Fri, 24 Oct 2025 23:28:58 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1625541431e60b63dee6b7509c5216b0f77698308637c2f69e10857633dfe446`  
		Last Modified: Fri, 24 Oct 2025 23:28:58 GMT  
		Size: 329.3 KB (329292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d074b4325544ab8e4db34178af765c9ec2cd72863df3a287e07b14ad6471336e`  
		Last Modified: Fri, 24 Oct 2025 23:28:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0a2f0fedb809910bb81f69daa8d455b8948983716de9cdecbb37fb0b825596`  
		Last Modified: Fri, 24 Oct 2025 23:28:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2970dae379b573a5e4f80f9eadc1b25a83b4eb67705183cbf1a2d7ca099d90`  
		Last Modified: Fri, 24 Oct 2025 23:28:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3ed3170f3350593b563a8d8e56efc74b9b725c4c8c6580aa170cd8a57bea49`  
		Last Modified: Sat, 25 Oct 2025 00:12:11 GMT  
		Size: 221.6 MB (221577055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04900c0e496bcc92fcc63605b98ac548959ebbd444f901583e797ee054fed778`  
		Last Modified: Fri, 24 Oct 2025 23:28:59 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
