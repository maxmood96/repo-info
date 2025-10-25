## `eclipse-temurin:21-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:3ebd7545b2938625078f5b12500cdef3979b5f11bec8bb194e1247da4c4007ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:3f7278bd3e30fcd2c78f7f3ac91fc21257f85daca9cd9aeff9805960f823fa25
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3601206140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5834f738f30fa529b3ee4513df11b2cc3deb2370d32edcf6e6a9b05b46c6ac77`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:23:18 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Fri, 24 Oct 2025 18:23:57 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.8_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jdk_x64_windows_hotspot_21.0.8_9.msi ;     Write-Host ('Verifying sha256 (d82030e8689b19efedfbce50ce38351ca81b302c06936584c6a27bda18339df8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd82030e8689b19efedfbce50ce38351ca81b302c06936584c6a27bda18339df8') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:24:05 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:24:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4b817687adaa375876765752435361cedcb186b49d3b6c48bede28ed9250f50`  
		Last Modified: Fri, 24 Oct 2025 18:23:18 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f66d98b00921e9c466ba325c126c905c43baf1ff7273df1f4adfeb0690b5935`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a35a6517ff92dd9a65386fbab6b073bd27e50b84d4e72aa569f89ef7881434`  
		Last Modified: Fri, 24 Oct 2025 19:19:15 GMT  
		Size: 380.5 MB (380497161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf928fac7f4809c50efab03cff0e233c366fab1c2c1c4e002c0906b568ab7a1`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 358.0 KB (358049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d576c9b7b352122f01fd64aa5a3de4b83592e851d0e9ce877771f0569d0796f7`  
		Last Modified: Fri, 24 Oct 2025 18:24:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
