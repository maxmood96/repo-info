## `openjdk:20-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:fabee277cd93eb14d93ebb7ae78d53710c170605937449188c96e696b6a1b180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `openjdk:20-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull openjdk@sha256:18ffd36bdac05c63225d1b661e13c3d0dafeebd4c2cfbc9d326dbc197326f1e9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2510485232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf15fbe6b22db9bcf8d7034c372c414c37a1a2d96749a1d602dbf7b5f8df823e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 12:11:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 16:55:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Aug 2022 16:55:00 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 10 Aug 2022 16:55:20 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Sep 2022 22:26:31 GMT
ENV JAVA_VERSION=20-ea+14
# Mon, 12 Sep 2022 22:26:32 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/14/GPL/openjdk-20-ea+14_windows-x64_bin.zip
# Mon, 12 Sep 2022 22:26:33 GMT
ENV JAVA_SHA256=9a074e380bbef6c389a660f1f21bf1cfc449cee8d6c387f4422305b2feb06dc5
# Mon, 12 Sep 2022 22:27:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Sep 2022 22:27:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a5e3787c778295a5877e0381020b02273a985f7db2dd483ddff586869546e4c`  
		Last Modified: Wed, 10 Aug 2022 12:42:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0cc935c154780815cf1fb6065aa1c262b52a7648b984b06133beb4e95833c0`  
		Last Modified: Wed, 10 Aug 2022 17:27:08 GMT  
		Size: 624.7 KB (624700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43525a703370320083aa7f64beeb4176b2090f555b73f9be7f9cb9fbda9f5736`  
		Last Modified: Wed, 10 Aug 2022 17:27:07 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf27aca426cd52616bfeb5296c1b75f2095211cf6c91d27a306c654522f65a32`  
		Last Modified: Wed, 10 Aug 2022 17:27:08 GMT  
		Size: 557.0 KB (557029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:183ea27befb7b75a74b9cab96551b9bbfa0c7751df06a28fa42efbd05560a830`  
		Last Modified: Mon, 12 Sep 2022 22:32:13 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3b935728d4fab1d3274f8f9f9ad5e299cd255c20b18d21646c3297741910be`  
		Last Modified: Mon, 12 Sep 2022 22:32:13 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b090efe8a6615c7523c30534cad5f24fb8d40f19aaf14f886bfccc47bdad8abc`  
		Last Modified: Mon, 12 Sep 2022 22:32:13 GMT  
		Size: 1.4 KB (1450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309b2ec559b86f6e4ec701c1e8429e31760fe4eed154f70fe95c7fc23f55f6e2`  
		Last Modified: Mon, 12 Sep 2022 22:32:33 GMT  
		Size: 192.4 MB (192405855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9746075a53ad1a28f5bbc17fd035f666b65380e362af8691b89cb366f11de290`  
		Last Modified: Mon, 12 Sep 2022 22:32:13 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
