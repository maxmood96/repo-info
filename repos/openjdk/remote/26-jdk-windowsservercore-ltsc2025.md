## `openjdk:26-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:a3ed7e66d3bba791dabd546aac8fd2e2ba5bbfd47b9132b83c0704defb2a9f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `openjdk:26-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull openjdk@sha256:ed9361982e7a2ab55baa38565159434bae17334cd8a49224c80d5aac69e737a5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3791516956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a72f8c30ad6f8717096f5795f648da31de3d843bd7918001a0d7f6fdc85d22`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Mon, 22 Sep 2025 22:14:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Sep 2025 22:15:04 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Sep 2025 22:15:05 GMT
ENV JAVA_HOME=C:\openjdk-26
# Mon, 22 Sep 2025 22:15:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Sep 2025 22:15:11 GMT
ENV JAVA_VERSION=26-ea+16
# Mon, 22 Sep 2025 22:15:12 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/16/GPL/openjdk-26-ea+16_windows-x64_bin.zip
# Mon, 22 Sep 2025 22:15:13 GMT
ENV JAVA_SHA256=f867e655606913a0bda0dd383b0d783722ba5b64b9fa63a7a684afb3ed9c5e0c
# Mon, 22 Sep 2025 22:15:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Sep 2025 22:15:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74b8b8b5a83a54167547465bd828d627063f249c2a0208a38b6634318bdd8b86`  
		Last Modified: Mon, 22 Sep 2025 22:30:19 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b304f9af9491b27084d8327d8760ca7ec01fb168caeeb21a7df8c8e493ccf094`  
		Last Modified: Mon, 22 Sep 2025 22:30:19 GMT  
		Size: 389.3 KB (389296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c08736d1d309df8187486c86b75207bbaa18f813e3e82395c5b0d5cdd0067f08`  
		Last Modified: Mon, 22 Sep 2025 22:30:19 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0305f5a163efcca170f2574545037761393b86d2b4e072a6aa1e22e12fe53c7`  
		Last Modified: Mon, 22 Sep 2025 22:30:19 GMT  
		Size: 363.1 KB (363095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5933456860f13654a6ea03cbcc40c26c6356c16e22a58b150200336bd926d55e`  
		Last Modified: Mon, 22 Sep 2025 22:30:19 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:217a93bf136fde55d5e45dbab9930df5d7d21bf34d317c5b7e8a5931c9995c20`  
		Last Modified: Mon, 22 Sep 2025 22:30:19 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79bad94beb242e0e5ad9c931d40a58192e0511ff57984607e0952ae41b47d45c`  
		Last Modified: Mon, 22 Sep 2025 22:30:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8f312eda5a61cb90744eaa96b1ec382764385f35f7da3ecda5945c107898559`  
		Last Modified: Mon, 22 Sep 2025 23:13:03 GMT  
		Size: 219.3 MB (219316932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102f5f05c526d43c45fa859790128af275bbfd027a038398652a44563a59c593`  
		Last Modified: Mon, 22 Sep 2025 22:30:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
