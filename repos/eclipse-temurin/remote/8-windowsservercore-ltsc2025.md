## `eclipse-temurin:8-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:7e3e8d9d8ad4d25f5430bd4cd196ccadaee3d15d2040209913a7c38a03b76668
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `eclipse-temurin:8-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull eclipse-temurin@sha256:76c3aed369b562891cdc97d22e82379ab9d27ca8157c22db1480f36778f03650
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692075279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b6b6545311cbf4bf46a87b37209404ec68436fb0472f6c29da39f90b9af135e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 31 Jan 2025 02:17:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 02:17:13 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 02:17:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 02:17:42 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b960189aaf2d6ccc538da7e09b9ae6f615a77bada8aef25e1d3ff85a533b1f`  
		Last Modified: Fri, 31 Jan 2025 02:17:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a71196af466734aa2973a863b990bd2f64de9c4c0d2fb655167e142f13211f`  
		Last Modified: Fri, 31 Jan 2025 02:17:46 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78903cb89d7692d47814c381c39f0e2c845603925fee5f7438b2449d1c186453`  
		Last Modified: Fri, 31 Jan 2025 02:17:56 GMT  
		Size: 191.4 MB (191402599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:496df0a47956d61bc1f85579cdac419e17d4399ef5cc5f3fca209be732590013`  
		Last Modified: Fri, 31 Jan 2025 02:17:46 GMT  
		Size: 392.5 KB (392497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
