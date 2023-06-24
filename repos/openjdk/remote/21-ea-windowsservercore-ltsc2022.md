## `openjdk:21-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:90140be1fd2b5d3e13ade554957524a26118df8b2edff6c0665346a148aee68c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `openjdk:21-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull openjdk@sha256:a9bc2bd00defa8a0dfa301ce8cd0ba53a471471382cf060bb2912da2b01365e7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1625120173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b6317f199fd5f9cb185cce5bba942bf6627998316e1879a6a8e4f989cf2bef`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 00:38:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 24 Jun 2023 03:03:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:07:27 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 24 Jun 2023 03:07:49 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:07:49 GMT
ENV JAVA_VERSION=21-ea+28
# Sat, 24 Jun 2023 03:07:50 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/28/GPL/openjdk-21-ea+28_windows-x64_bin.zip
# Sat, 24 Jun 2023 03:07:51 GMT
ENV JAVA_SHA256=cf31047fdf44c7303408c4868c810af10ec573e926925041e621f0d5acca4583
# Sat, 24 Jun 2023 03:08:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 24 Jun 2023 03:08:44 GMT
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
	-	`sha256:4eec6f45c20e189779c1a14ac267c15e9db3eefe85034e40b6f92372759a288a`  
		Last Modified: Sat, 24 Jun 2023 03:14:21 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb14372fe1d2fbfda13afae0e93eb2611308220211945e4daea088ac9989f16`  
		Last Modified: Sat, 24 Jun 2023 03:14:22 GMT  
		Size: 262.8 KB (262765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869df31a3297f47245f24644db804b87052e167ca814c38607b9c0fe307be50c`  
		Last Modified: Sat, 24 Jun 2023 03:14:20 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f0aa33d5bed85ad23deb10de330e5f0bdff672f0059dc084fda4699d7e0584`  
		Last Modified: Sat, 24 Jun 2023 03:14:20 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19b890d99cd3820f9ba63cc332a38719a17bb0446377756d6f827b458554d824`  
		Last Modified: Sat, 24 Jun 2023 03:14:20 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f6be8178551a27e534f8aed7c9fa95517e8fae7dd9e5632c3f35cffd9866bb5`  
		Last Modified: Sat, 24 Jun 2023 03:14:41 GMT  
		Size: 198.2 MB (198231930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88bf66288ddd519e2329df75f7f31ce46b87af8731d5767feb9b7ccb6ffeb9b2`  
		Last Modified: Sat, 24 Jun 2023 03:14:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
