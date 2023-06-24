## `openjdk:22-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:0bc6c6492436c5b24634b24b70e70b340a298fc4fdc9241f5b4374b2e5b2bbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `openjdk:22-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull openjdk@sha256:2042ad2d61913adac959e00cc5ff71468961ed97919826aed2c5d8adebcd3191
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1625921315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a145ac3f0822b0680c20b4237680645db995e6b9f44032f1db8c1eca639022e3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:03:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:03:12 GMT
ENV JAVA_HOME=C:\openjdk-22
# Sat, 24 Jun 2023 03:03:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:03:37 GMT
ENV JAVA_VERSION=22-ea+3
# Sat, 24 Jun 2023 03:03:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/3/GPL/openjdk-22-ea+3_windows-x64_bin.zip
# Sat, 24 Jun 2023 03:03:39 GMT
ENV JAVA_SHA256=9f49c43ec99bd9d9c8035adc143088b1eb688cf9c67de5cf015a43723a0a7b39
# Sat, 24 Jun 2023 03:04:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:04:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27db350c833f7fe0378bc977cd819c1ffe4133ff02ff69f1531f8ddc552c2366`  
		Last Modified: Sat, 24 Jun 2023 01:15:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5de10d117b5ef80c7852b0714d37536955d84892882d5f3f97a4d53631493623`  
		Last Modified: Sat, 24 Jun 2023 03:12:27 GMT  
		Size: 318.8 KB (318813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42164a02c7f5d71bd26777e64b91b0bd8307f2753488ee14e31eb3bf123f1815`  
		Last Modified: Sat, 24 Jun 2023 03:12:27 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:300b25e7f376e2eb14f637c2bc345eeb47edb02cc31dd17445ef2acc2140c0ff`  
		Last Modified: Sat, 24 Jun 2023 03:12:27 GMT  
		Size: 262.6 KB (262553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d8576e40624ef0f913c2fa0c09bbfa9b9c3adda7bbf16f56263f32590880eb`  
		Last Modified: Sat, 24 Jun 2023 03:12:25 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3539b7a81e3bfd37152732e45a4739c34b753d7c2ab24be92abddbf7c8e832`  
		Last Modified: Sat, 24 Jun 2023 03:12:25 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9b16e2cb59c119e379213234f4cc8731ff67ce192d069b27a2cb718cbd30d9`  
		Last Modified: Sat, 24 Jun 2023 03:12:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d123ac570b0048d0a39bf897c247e433085080f02263f1b983788c243cd751`  
		Last Modified: Sat, 24 Jun 2023 03:12:45 GMT  
		Size: 199.0 MB (199032954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c981b736d50c859d3562c6adab5a80b19307d22cffe4e7a6226b4688219def39`  
		Last Modified: Sat, 24 Jun 2023 03:12:25 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
