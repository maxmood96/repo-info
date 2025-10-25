## `eclipse-temurin:8-jdk-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:6c1515aeedde5cdf4a1ccef4b4e182d88943801e2311c59342754cfefbe19694
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:8-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:3036ba90f73961caf4d07661ab96ceae439ff95d344f6da969bbc56f3a3f9ee5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3411997761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:157d9e1b486854434f135519662b32018c0e97cd88c3082795c8b2be0c624915`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:13:15 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Fri, 24 Oct 2025 18:13:50 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (6abb1058eb80b3ae13f63cd7aef302724aebaf0a68924fee6a503ff4a0a39901) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6abb1058eb80b3ae13f63cd7aef302724aebaf0a68924fee6a503ff4a0a39901') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:13:56 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
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
	-	`sha256:538fa5a72d17bbf02682b93a31bb1c51e26fa76d63e779418172290659f96331`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83fe3c9595c37dac23e58be55601eb71a611353db97c215fe7c2f843aaea4298`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44003a7a9c9cc84e9a6eddd7e5d342af4fea376658ab6521f6089feeb96d398f`  
		Last Modified: Fri, 24 Oct 2025 19:15:07 GMT  
		Size: 191.3 MB (191285298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc64f0c278c71cef2ece0f249b1447e0a1268df793a0aeb2f97cb139fd393ef`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 362.9 KB (362867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
