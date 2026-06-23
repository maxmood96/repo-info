## `openjdk:27-ea-27-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:e7b7baa3b4ca73f61e93ed4d327cef01fad0d4603f86481bfb729fcdf1058569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:27-ea-27-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:45977a26545a29827dce031dc4558116165ea1301f6625da1004a5616841555c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2503478433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de4255d17527c24f1bcf6ed3372a6f5a45a370f559f9cb2bd796c7a734313493`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Mon, 22 Jun 2026 22:44:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jun 2026 22:46:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:00 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 22 Jun 2026 22:46:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:08 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:46:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_windows-x64_bin.zip
# Mon, 22 Jun 2026 22:46:09 GMT
ENV JAVA_SHA256=95f2039dcf26a1c012aaa98a839b7c4ccc5974f9697e6d7c7c6a332afcf12fed
# Mon, 22 Jun 2026 22:46:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8323c80a7f544f650118cc07ff573d79bad528c94c6994476943c1271d2034dc`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989b1f39645f7cd91f59249046be9d11f03fb07c9d5b80536e11fa92b277491`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 407.5 KB (407468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3438329670602264a5199cbb1f0f59ebd0ea2e0049db69feaa625544d6b8e07c`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4264cc044190a364f24d7c456b64463f73c511c93c435d3db64b2841d1d87af1`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 396.2 KB (396227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dfe1bd813aa820de4fe9c0833a7859ccd6e348c2d626a4e55cd97e00dcba17`  
		Last Modified: Mon, 22 Jun 2026 22:46:46 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8205d8e3476e38c1d17952dd9443012cab97be6f337d69e3b81f8e38fbd2a9`  
		Last Modified: Mon, 22 Jun 2026 22:46:46 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e7cc44e40eaa03fadb796a5c65af5960f5a52e14fd0c017a7becd085c9f036`  
		Last Modified: Mon, 22 Jun 2026 22:46:46 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bf9e65e6701b000df86b196168ff3135c3b5c1e649da72f33e3db18cefbb0a`  
		Last Modified: Mon, 22 Jun 2026 22:47:02 GMT  
		Size: 223.5 MB (223523980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bd05d57f03696d008da55bb6127c5157ac28bddf478a82ff84ea7677d1aea9`  
		Last Modified: Mon, 22 Jun 2026 22:46:46 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
