## `openjdk:25-ea-18-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:73529a8d957f205724d1aaf9d780a45897216781de6716ae67f5eed736bb2780
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3453; amd64

### `openjdk:25-ea-18-windowsservercore-ltsc2022` - windows version 10.0.20348.3453; amd64

```console
$ docker pull openjdk@sha256:a8cbe5a83fd2c8a7bffb59b4c545c7b7d162a95deaa055da837fabdbdd45b597
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2479666258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9f08faaef7f0fa1eb27155a7e25f489113adbe436d81f570103b837a098ed9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Mon, 14 Apr 2025 23:03:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Apr 2025 23:03:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:03:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 14 Apr 2025 23:03:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:03:33 GMT
ENV JAVA_VERSION=25-ea+18
# Mon, 14 Apr 2025 23:03:33 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_windows-x64_bin.zip
# Mon, 14 Apr 2025 23:03:34 GMT
ENV JAVA_SHA256=41f24482b5d173e5a8f242d81909835bd7e85fdb131b901bff9a150186c3c03c
# Mon, 14 Apr 2025 23:03:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:03:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144f12c177739096ac6703a44526030560394b9864781248bef35f91d8ee1f12`  
		Last Modified: Mon, 14 Apr 2025 23:04:02 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3a1eca3f316080aac6c64cb8ada843b52617a71b7ded70271deaf5ac13dfc21`  
		Last Modified: Mon, 14 Apr 2025 23:04:03 GMT  
		Size: 358.9 KB (358855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84edcf4155c652365e893cc33ec447bfe4d527351ee0c671a6e335f7305f9992`  
		Last Modified: Mon, 14 Apr 2025 23:04:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7b8fcfb4d81cc41cc0ff633ccef1f341147312d248d78ea8dc83af65aab936`  
		Last Modified: Mon, 14 Apr 2025 23:04:02 GMT  
		Size: 346.7 KB (346689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:557ac4c52496258109a462055bb88ff225efad1f3fc4041fa1a77538f7ef9930`  
		Last Modified: Mon, 14 Apr 2025 23:04:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d992152ae40e2fb0a1914b06ca07b9ab2b90a20640266e20aa9f255265de0dcc`  
		Last Modified: Mon, 14 Apr 2025 23:04:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a91c4ee81a97e60912dc2229b0693227f98a6a22d54e0cfcbe9efba703ec846`  
		Last Modified: Mon, 14 Apr 2025 23:04:00 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbaa182ef67c0eb539b55a36022b49c01f8c843959c19c2bcd1f4146e53e33a`  
		Last Modified: Mon, 14 Apr 2025 23:04:12 GMT  
		Size: 208.0 MB (207957255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e236b022a026ae874b9b8f92aff1d41cdc662e752d12f6ce06659390e896adb`  
		Last Modified: Mon, 14 Apr 2025 23:04:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
