## `eclipse-temurin:8-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:9d110e11150ad434339bb2c073d9919b97c9e9e7a59cf9d24e1ab3cd486e5a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull eclipse-temurin@sha256:cd2e7a97196d62d28ca07e04568ef915c52aa20f89ec06770e686d1357267d9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037045373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d834f3a619e94635a44355fb7f292a38214c8919d25e679d59254c722fad1a1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:53:21 GMT
ENV JAVA_VERSION=jdk8u482-b08
# Tue, 10 Feb 2026 22:53:38 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u482-b08/OpenJDK8U-jre_x64_windows_hotspot_8u482b08.msi ;     Write-Host ('Verifying sha256 (4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4e0dbdff6537f43b012e2376de59845968afc99f5901303a28a881b42d93d795') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 10 Feb 2026 22:53:43 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fcfd35fb91d5c96c95008501f15273667b38b3c34c813a77275adb8e4064973`  
		Last Modified: Tue, 10 Feb 2026 22:53:48 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4578e737ca97fc2098d4c2f88fc46f3dd3ce9473f2cc986ab1b0389e911f22`  
		Last Modified: Tue, 10 Feb 2026 22:53:48 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ab05c1d6722e4634b510cecbb24fe709c929992160193a200483222944342c`  
		Last Modified: Tue, 10 Feb 2026 22:53:53 GMT  
		Size: 71.9 MB (71936071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1990c4865a76722ce3eb890d85ae7d24549e1eeb9388071ae6d2f662f3d776e`  
		Last Modified: Tue, 10 Feb 2026 22:53:48 GMT  
		Size: 346.8 KB (346805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
