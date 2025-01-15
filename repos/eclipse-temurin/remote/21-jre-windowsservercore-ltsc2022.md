## `eclipse-temurin:21-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:fec1b30ba625cd40b5cafd0d3dfbe254dd6da18ed266bd462c140282fbf3ed61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:6a87cd02888e94bd2f17192aba5f1626c3c9a676c071b5ce1246fbbdf1f2c378
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2347034113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ed609475e3a514ff50cfba48c967b726e6853a1b611a8ce41a60c1590733db`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:34:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:34:52 GMT
ENV JAVA_VERSION=jdk-21.0.5+11
# Tue, 14 Jan 2025 23:35:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.5%2B11/OpenJDK21U-jre_x64_windows_hotspot_21.0.5_11.msi ;     Write-Host ('Verifying sha256 (baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'baa356843cbe2cbc8e49bad1cfef27eaaf5e59748a1627be40492804753c706a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Jan 2025 23:35:20 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78d02b7a219d362045a9edc30f12fe39416f1a558f25881eb9b62a3f70d88f4`  
		Last Modified: Tue, 14 Jan 2025 23:35:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:407e34d9ae021673ae6dc7429659626c09582e211852ec8cde9bbbfe455b230e`  
		Last Modified: Tue, 14 Jan 2025 23:35:24 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e385a2ae6044cf9f5ffe6b913db15118def9cee794c050b5647c71de71b7399`  
		Last Modified: Tue, 14 Jan 2025 23:35:31 GMT  
		Size: 84.3 MB (84293681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:149632165d680f73b7cdfa6b2bac87bf976b994a916d8400976f56a5c241f5c5`  
		Last Modified: Tue, 14 Jan 2025 23:35:24 GMT  
		Size: 352.6 KB (352608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
