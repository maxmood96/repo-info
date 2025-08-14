## `eclipse-temurin:17-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d1f00ab92d0b01be3c245e4fa92ddf45eb614bb08c9207a70c9eec270d3fcc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:17-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:24826df2600f7fa1736bbccd5fd68645b231624595146a91e749a52829db1169
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3854436946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4041a8473308a7a6ac466ec670bbe7af462a70da766e1df7b18f60b0beec806`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:00 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Tue, 12 Aug 2025 20:27:19 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.16_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.16_8.msi ;     Write-Host ('Verifying sha256 (1c3701f074d75036650731bcf6b08d69b1e3567bfa853f0ddd7aaba44da5b595) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1c3701f074d75036650731bcf6b08d69b1e3567bfa853f0ddd7aaba44da5b595') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:27:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:27:25 GMT
CMD ["jshell"]
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
	-	`sha256:fa39133f320a3101f43ed8ac51aaf78825657a2bbc4cc6efb8cdf2533e5d618e`  
		Last Modified: Tue, 12 Aug 2025 20:31:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b2163d898791653c57474ad505c4f11c984eef809cbacf84384301bef76137`  
		Last Modified: Tue, 12 Aug 2025 20:31:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb7b78f21f390a110c8d13965a8ad6a1e68632b3fb215825be79634bf0fbf92`  
		Last Modified: Tue, 12 Aug 2025 20:45:43 GMT  
		Size: 355.2 MB (355237054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc76b26d881bc0f3e9492529a276a4b8510077c8bc0e0aa820c3356922d162fe`  
		Last Modified: Tue, 12 Aug 2025 20:31:18 GMT  
		Size: 365.5 KB (365541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58421e6aeb7608493cbd80b9e9f5c1eb4326451a3c5454cb19df3d50f4ada36`  
		Last Modified: Tue, 12 Aug 2025 20:31:18 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
