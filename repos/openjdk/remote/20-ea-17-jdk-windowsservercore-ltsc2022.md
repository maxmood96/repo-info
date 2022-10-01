## `openjdk:20-ea-17-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:3c63ac66302f54e3210278f915c67aefafb5fd178f6cc932b609cd95bf782623
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `openjdk:20-ea-17-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull openjdk@sha256:4ed78ee31756e0f8d488d4f3ac311d6303537f776acc574fa41930efa8c8f293
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2540509155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27de124f0a76c8109c0cfe63fe17ea33147317adc7615e1de436e3f8b3cfc6c7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 17:03:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Sep 2022 17:03:53 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Sep 2022 17:04:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 Sep 2022 23:23:35 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:23:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_windows-x64_bin.zip
# Fri, 30 Sep 2022 23:23:37 GMT
ENV JAVA_SHA256=aef462584419d1a928f1225061ce4e999d225d636a1406a805962af82e5ca877
# Fri, 30 Sep 2022 23:24:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 Sep 2022 23:24:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6298a3366175cd1297fbed9781ab93da075956d0549ae06cc0ad3a9f0759b9`  
		Last Modified: Wed, 14 Sep 2022 17:21:32 GMT  
		Size: 593.4 KB (593387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69130dc68926a7dd74a45c56d76c52a89dea16ac92d70aab946e32f9bddfce3d`  
		Last Modified: Wed, 14 Sep 2022 17:21:32 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fc7fa67a5ff75b4568b1c4ae7e98ea07d91433bfd85d115fab3f9d9fd1c762`  
		Last Modified: Wed, 14 Sep 2022 17:21:32 GMT  
		Size: 525.0 KB (524965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067c9b30423cf3eff116bcb14c82bf9aba7f415eb78337d127ad3b404eb4c9f8`  
		Last Modified: Sat, 01 Oct 2022 01:16:44 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddd728e95d6edf8b452d324ddc7abc60297b17123871ef6c98ebc7d7d2602`  
		Last Modified: Sat, 01 Oct 2022 01:16:45 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cc174cfa9936d5a34e13cbed7ccf47389cadf58e5e117f0ea03a4887c4ac15`  
		Last Modified: Sat, 01 Oct 2022 01:16:44 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de38b7b62801bf31fc4a3883088461922441c0ef938568aae8c950e966624a4`  
		Last Modified: Sat, 01 Oct 2022 01:17:04 GMT  
		Size: 192.4 MB (192432787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7741199c6e12af8e4d50ef6d9312a222d7b369817a71783f000407086fa7f47`  
		Last Modified: Sat, 01 Oct 2022 01:16:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
