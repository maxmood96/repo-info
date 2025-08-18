## `openjdk:26-ea-11-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:e0d168895b6ae4e4d1306c8d302eab8a4da521327f669eeb760818120efe97cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `openjdk:26-ea-11-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull openjdk@sha256:2b767e8f206fb9d316dd4f0daf575103012bb305b91519411cf5359a33879a00
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3718626003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49e3e00ac34bdcd755803bc48d70edc8f912edd891d711f496d9380eb7c47d7c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 18 Aug 2025 18:19:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Aug 2025 18:19:24 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:25 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 18 Aug 2025 18:19:30 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:30 GMT
ENV JAVA_VERSION=26-ea+11
# Mon, 18 Aug 2025 18:19:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/11/GPL/openjdk-26-ea+11_windows-x64_bin.zip
# Mon, 18 Aug 2025 18:19:31 GMT
ENV JAVA_SHA256=64e5c9fa2194c4b3cd3b424b1688dd4a30f7cb8e9b1b837030e835cfa5d8d866
# Mon, 18 Aug 2025 18:19:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 18 Aug 2025 18:19:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00f4769a39e30282a3a2110e483c85c4904fcf6a48181294f031fe4e1b4cb07`  
		Last Modified: Mon, 18 Aug 2025 18:27:17 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c199fb60e8499521fff8df55b8bc0db1e05eb0222f6af4f8893529be4fbac793`  
		Last Modified: Mon, 18 Aug 2025 18:27:17 GMT  
		Size: 391.2 KB (391206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34b8f1a3e7f83885aaeaf7779f3bd5cb9c87bbb73c7395fd9a5933aab237015`  
		Last Modified: Mon, 18 Aug 2025 18:27:17 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7dcc65ad42c7f2045bb455e234829d9d37cdbcf7d339562860e8404888709db`  
		Last Modified: Mon, 18 Aug 2025 18:27:16 GMT  
		Size: 370.0 KB (370028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628bd34e5b5d323434dc19dd99591665ba5f2e59eeef9e286c1419b8f483c3be`  
		Last Modified: Mon, 18 Aug 2025 18:27:15 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:001dfa7771828da09db15f86cb4add9bf711802ef0c9ffa25160c987a4d4aff7`  
		Last Modified: Mon, 18 Aug 2025 18:27:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195f3aa959d9af6f8cf1e0344ddaafe415a6c3c259d2e3f68a12205ad6cf81a5`  
		Last Modified: Mon, 18 Aug 2025 18:27:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:324eb6505e267031e7215fe9086b5ff42f3579f7dc93180688db9405396393b3`  
		Last Modified: Mon, 18 Aug 2025 19:08:52 GMT  
		Size: 219.0 MB (219026436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4202e3fbad5ddb083c14381209627ffcb4e395b4b295a6d9f400f955790ae0aa`  
		Last Modified: Mon, 18 Aug 2025 18:27:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
