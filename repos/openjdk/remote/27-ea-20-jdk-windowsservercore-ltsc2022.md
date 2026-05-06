## `openjdk:27-ea-20-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e13604a303e1542d557b48e4245f856a3e692d33fe52731da48e13ed1f8c6de5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-20-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:3af02388d6ecb2961378b5310ca4f7e0156b9809d23b49b3e721f356c06cc6b6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296019714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b573c0573f6c3f33ea3f0b84af944ae4a9128415aa2181aedb3b987f640d3a2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 05 May 2026 23:00:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 May 2026 23:01:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 05 May 2026 23:01:14 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 05 May 2026 23:01:23 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 05 May 2026 23:01:24 GMT
ENV JAVA_VERSION=27-ea+20
# Tue, 05 May 2026 23:01:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/20/GPL/openjdk-27-ea+20_windows-x64_bin.zip
# Tue, 05 May 2026 23:01:26 GMT
ENV JAVA_SHA256=5499df903e0ea0fb9652da36292197a89324f03f18fc670d4af55d54c5a75687
# Tue, 05 May 2026 23:02:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 05 May 2026 23:02:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdd9ce40371c9ec789b1e772bfe08819d562afa0f8fbe3276f8ee03e83a1868`  
		Last Modified: Tue, 05 May 2026 23:02:15 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59be0aa233d1cdefb8d3fd8dcdb843328246ebd8c9fdb0941c1ba4f5cab4345b`  
		Last Modified: Tue, 05 May 2026 23:02:15 GMT  
		Size: 482.3 KB (482258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac8488ea48fdcea8f7619f864416279171be676eaed46228d874ea79582e5db`  
		Last Modified: Tue, 05 May 2026 23:02:15 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4815d4fca2874e3b889eabae82e0c6f506f7daca18d13434eeb4e6f8714c7e`  
		Last Modified: Tue, 05 May 2026 23:02:15 GMT  
		Size: 346.3 KB (346280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e68c476df70ad4687debb73a565344599aa5064bed353a750e0f0683593e80`  
		Last Modified: Tue, 05 May 2026 23:02:13 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c0be45a7b1d5ab4d4a4457c0db5cfccf06945b5aa3e456b5115abfb2e38967b`  
		Last Modified: Tue, 05 May 2026 23:02:13 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe359530f00788995b7e61f0a43ae08fd38d05cd86f862a0600e46aa91f1ed3`  
		Last Modified: Tue, 05 May 2026 23:02:13 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111b49a5d55a11d68f593a8d6b6bb3ba15c48cd6de91f962d8768ec8fa9a7490`  
		Last Modified: Tue, 05 May 2026 23:02:29 GMT  
		Size: 225.0 MB (224972026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc57782d1b5b62efdbc1ca6fd42cc92a68dd0985d1ca393df86a86d6aa0295c9`  
		Last Modified: Tue, 05 May 2026 23:02:13 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
