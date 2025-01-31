## `eclipse-temurin:8u442-b06-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:89b71c23960602d272843e0cb2ad8ed4f394a2a652ded938ebaceb5e540e1b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `eclipse-temurin:8u442-b06-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull eclipse-temurin@sha256:a8686a5c3087f8e5484954a16b91a5d366a1e8662a616ae8dbfeaeaab4bf0210
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335478783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5116ba652eba17be48040cdc52cc89775528ad2df4f4af47223b365bce3d1d07`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 31 Jan 2025 02:12:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 02:12:24 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 02:13:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 02:13:48 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:45f66911505f212637c9f4ba4931de7ef8073b1b0d7b4dac80383115f19598e5`  
		Last Modified: Fri, 31 Jan 2025 02:13:52 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d4dd320901d1f5f5ec73aabba75b92553bd26429015910fd83ba62575b76aa8`  
		Last Modified: Fri, 31 Jan 2025 02:13:52 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565fd3e538266485d74ba4c71d8103030015bd391e174ebdf8339968fc74f43a`  
		Last Modified: Fri, 31 Jan 2025 02:13:57 GMT  
		Size: 72.8 MB (72763963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c44c5fced4efe9bf6f2c715a5aba16765a9981d442a94342ac650b38eda41a`  
		Last Modified: Fri, 31 Jan 2025 02:13:52 GMT  
		Size: 327.0 KB (327012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
