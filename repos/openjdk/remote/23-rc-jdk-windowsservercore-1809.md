## `openjdk:23-rc-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:dd65ff2cedb65075e7e970242a1a1df0a0b2adbe0f7f9106e35095711cb4468a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-rc-jdk-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:5f24c3eaf9f83a0373d4976784e9dbf8f4ceae066f61411b8fa660a15f543d26
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445676504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128cc257453e32c23c5f11f7efcbcb6d0b402f67982a27cf04c05b7cd8b2ff11`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 12 Aug 2024 17:58:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 12 Aug 2024 18:00:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 18:00:20 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 12 Aug 2024 18:00:40 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 12 Aug 2024 18:00:40 GMT
ENV JAVA_VERSION=23
# Mon, 12 Aug 2024 18:00:41 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk23/3c5b90190c68498b986a97f276efd28a/36/GPL/openjdk-23_windows-x64_bin.zip
# Mon, 12 Aug 2024 18:00:41 GMT
ENV JAVA_SHA256=b18897bec6b1c6e0f639d95757eb0e3b0ec3d69720f6e4631874f2f9408075c5
# Mon, 12 Aug 2024 18:01:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 12 Aug 2024 18:01:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0485a52b2750c5edb17d3e85e3529319914f5b22cf8753766e55ee20f3ec11eb`  
		Last Modified: Mon, 12 Aug 2024 18:01:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee8b218b15bb28346580cc025ad46cf8bd48e0b5f561b9fb420a13326b3658c`  
		Last Modified: Mon, 12 Aug 2024 18:01:28 GMT  
		Size: 488.7 KB (488659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95d59080640177d6c33655e895233c773a865c183f452b6b89323d832196d22f`  
		Last Modified: Mon, 12 Aug 2024 18:01:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33acef4986e1e973579075c0e3092c491897e0d32a87c3ba740154d6e9d356c7`  
		Last Modified: Mon, 12 Aug 2024 18:01:28 GMT  
		Size: 332.3 KB (332262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:433fda61ae3b2a8228a886b1796366b5c46e36065bb4b8735b7f3f97daf05cb4`  
		Last Modified: Mon, 12 Aug 2024 18:01:27 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d398a322c8bd668f7e6178eff7ee8fe86a5689f3a469ad0a129081ff958cff18`  
		Last Modified: Mon, 12 Aug 2024 18:01:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a41fd79f637eb5202ef4f323f815caeaa80569733f6a50e58092627d06bb1d3`  
		Last Modified: Mon, 12 Aug 2024 18:01:27 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:534566af8484c380ad5fc3a1178e8b4f3d25823ea358b7988ec9abdd7013dd75`  
		Last Modified: Mon, 12 Aug 2024 18:01:37 GMT  
		Size: 206.4 MB (206418401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e905f3ed9d1ae9b89f53d995b8c4168eead00609a3819b1ad3d779f98d96c2d`  
		Last Modified: Mon, 12 Aug 2024 18:01:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
