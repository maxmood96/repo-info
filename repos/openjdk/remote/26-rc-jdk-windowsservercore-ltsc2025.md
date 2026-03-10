## `openjdk:26-rc-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:b52ee1847f264988ca18c05d1a3f3e411f2d9777f6fb22d532882fd7dddfa1d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:26-rc-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:2561d9bdf2cff7e17e2467cb1d4955cc915300b95d00f45e86835a294ad0a930
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2306230739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbb7d9327a2e96065c1641dbb816ea1d6f32a6221943dc5ad91a7121d14572f5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:57:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:08:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:19 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Mar 2026 22:08:25 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:25 GMT
ENV JAVA_VERSION=26
# Tue, 10 Mar 2026 22:08:26 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/35/GPL/openjdk-26_windows-x64_bin.zip
# Tue, 10 Mar 2026 22:08:27 GMT
ENV JAVA_SHA256=2dd2d92c9374cd49a120fe9d916732840bf6bb9f0e0cc29794917a3c08b99c5f
# Tue, 10 Mar 2026 22:08:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:08:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577b380a809fd7aaebdd6a6f0d59a090ff85fbb58921f36c06a704c2d76bade1`  
		Last Modified: Tue, 10 Mar 2026 21:59:21 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0156b576e3f86f67015b3c0b6524b34c8654c1cb0aa722b7bae4deee923477e8`  
		Last Modified: Tue, 10 Mar 2026 22:08:54 GMT  
		Size: 354.6 KB (354650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8ed652983feb31e1e377de8c767bee27f949667d3afd09b3402f77b9f2a285`  
		Last Modified: Tue, 10 Mar 2026 22:08:54 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b81457d6213b580a56c5a0e968d2018a286cba3e4bc5409e1f5c52c1464f448`  
		Last Modified: Tue, 10 Mar 2026 22:08:54 GMT  
		Size: 341.7 KB (341716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcfda05b5649db709e92356c4223aafb17d1c2751e65a83c038a9a0fa866feb3`  
		Last Modified: Tue, 10 Mar 2026 22:08:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b1a39f11bed4de14f1c9653ef6d31af8213014360bc7da12cc81e4d16c0bca`  
		Last Modified: Tue, 10 Mar 2026 22:08:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd57495802692f632d180dc4605bc6c4d899de2a85884f600a44216ce8be5733`  
		Last Modified: Tue, 10 Mar 2026 22:08:52 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7505c1be3c4c6627d42475429a95b9ab4e34c051a48802421b24729afd08fb61`  
		Last Modified: Tue, 10 Mar 2026 22:09:08 GMT  
		Size: 224.3 MB (224330498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5821cfd70ef24ca9efb3a59dfaec145a1eef550e0540c2e3142ccd7c2298cc`  
		Last Modified: Tue, 10 Mar 2026 22:08:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
