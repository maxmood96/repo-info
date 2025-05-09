## `eclipse-temurin:8u452-b09-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:0996c9c8cfefb5c569a7b52c05071a6a08b038705d0d4f5baabc65227c6ef819
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:8u452-b09-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:d7fda6f2ff8302d94203b9474ce624203e423b966300c7d2c4f7955af009aa48
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3468340470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1954f416d7859cd155acf9dc77e9e1db1686523acbc753479657628f4cd0891c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Mon, 28 Apr 2025 20:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 28 Apr 2025 20:13:07 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Mon, 28 Apr 2025 20:13:22 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Mon, 28 Apr 2025 20:13:32 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67762a71087cf37e2d6ec32f2dd038d35cf51694cfc253e4145f6f2e36018ae3`  
		Last Modified: Mon, 28 Apr 2025 20:13:35 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd7d144a858caca30f0d9c8958ec1e14e2e4aa08e04adb1dff7965891bcf41a`  
		Last Modified: Mon, 28 Apr 2025 20:13:35 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6265a92f6b2c3e61f70fd05f0ef20db995c55a307d80ee51147802dc404c219`  
		Last Modified: Mon, 28 Apr 2025 20:13:41 GMT  
		Size: 72.8 MB (72790019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e247ba03a79692013f7cdf54d811f82c5b374db8964ef33015b34344d3a1be`  
		Last Modified: Mon, 28 Apr 2025 20:13:35 GMT  
		Size: 386.3 KB (386342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
