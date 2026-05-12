## `openjdk:27-ea-21-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e8f55b2628ad7755b2064f01405a229c9ba70a6eaad6b26828d01adbc7e1749d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-21-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:01187c3e503ea42c18fd6031650f8e93a2acf9608e94a60a8c1a19c084901418
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296230036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f532b9869c61e13f3dd4c4e90ec635614175e8137f64824e546f48ed51a6e66`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 12 May 2026 00:15:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 00:33:32 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 12 May 2026 00:33:32 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 12 May 2026 00:33:39 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 12 May 2026 00:33:40 GMT
ENV JAVA_VERSION=27-ea+21
# Tue, 12 May 2026 00:33:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/21/GPL/openjdk-27-ea+21_windows-x64_bin.zip
# Tue, 12 May 2026 00:33:42 GMT
ENV JAVA_SHA256=c141a4db38b2d45883ed5d65a72f4444d1efa690d650027308594335dec2b07b
# Tue, 12 May 2026 00:34:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 00:34:23 GMT
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
	-	`sha256:fa492a5535facf20fd9ea86ddfd2827b386ca74f28e0073a7b036eb7144c3259`  
		Last Modified: Tue, 12 May 2026 00:17:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5772b261a4c5a975fe1d657ae1eadc601ec02136546c380096e456d196ba86be`  
		Last Modified: Tue, 12 May 2026 00:34:31 GMT  
		Size: 504.0 KB (503958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89cc1f33ae9f3dea7a86dbeb11177b6c3900d61941391c7e3ca6305728225ae3`  
		Last Modified: Tue, 12 May 2026 00:34:31 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02fea60138e87b095c50fb9b289baaed3fe76d7a714d951db769ba9d34946c11`  
		Last Modified: Tue, 12 May 2026 00:34:31 GMT  
		Size: 351.0 KB (350985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729914896d2d1d4c7004e00e50b373ce339c7b1dac5a789ee590a1641abcc902`  
		Last Modified: Tue, 12 May 2026 00:34:29 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be735ce1c172e122d8f19c339a99452ff5af2c099d72ffe125af7ca2c1ee6a85`  
		Last Modified: Tue, 12 May 2026 00:34:29 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf0c36114160f5d9b2c058b2477406e3a3050100227fde571eb0859698b1d1d`  
		Last Modified: Tue, 12 May 2026 00:34:29 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bbf01946aa0221b3da1a858d9a56e1bed67aa751a5053a2fea2cd27ccd81fa`  
		Last Modified: Tue, 12 May 2026 00:34:45 GMT  
		Size: 225.2 MB (225155938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2c436ef2d4451546d38f5d647ccae7726388f2ced06ef22f621d9721b5deda2`  
		Last Modified: Tue, 12 May 2026 00:34:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
