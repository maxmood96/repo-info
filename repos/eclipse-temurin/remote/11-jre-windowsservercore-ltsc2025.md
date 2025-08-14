## `eclipse-temurin:11-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:a5cabe4c8e5b42b118ebacee080a5fd0e243c883b314675d3ac9e4a2e214500c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:ff5e52400e828f4c93ce80cca410a6eb744b5080f4010e13d96cbe7f94768142
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3574130814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d1180814b6adcfd4d6ed65f438e95d5b15af4408f8cb6659a6d4e428748604`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:02 GMT
ENV JAVA_VERSION=jdk-11.0.28+6
# Tue, 12 Aug 2025 20:27:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.28_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.28%2B6/OpenJDK11U-jre_x64_windows_hotspot_11.0.28_6.msi ;     Write-Host ('Verifying sha256 (a093e7c3b7754bcf61140764eddb11343e3810890dcc3b96195b7d695cd1358b) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a093e7c3b7754bcf61140764eddb11343e3810890dcc3b96195b7d695cd1358b') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:20 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:332919e2fe9d03e978fca81fbfc7ce0a55ccc651ec7fe12a3359adf27180cc5f`  
		Last Modified: Tue, 12 Aug 2025 20:31:04 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c09745e2a304ab4e35127d54012f1bbf2f1de5be9b33b16cde9d63a8687cc4`  
		Last Modified: Tue, 12 Aug 2025 20:31:03 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf064087ede68cbe972ffc0431a65e44f23c7a2149ba3a877a5c46591e9c409`  
		Last Modified: Tue, 12 Aug 2025 20:31:12 GMT  
		Size: 74.9 MB (74923903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc60ad06a37db5549bb8abf8ed0617ae2922bae6a017e94ae89028765ddae743`  
		Last Modified: Tue, 12 Aug 2025 20:31:03 GMT  
		Size: 373.9 KB (373865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
