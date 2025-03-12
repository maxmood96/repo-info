## `eclipse-temurin:8u442-b06-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:84a3a393943bd1a3be46cef584172a14256cd88aa7983e9a80e673a33ee23a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:8u442-b06-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:3d7616ef733de3e68a1e54687d20c8ea868120ce77a6cb6b149ec71b081aace7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2981809353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75179d26c3029f04df99b0f3628d48132004c16bebfc4efa15a848f30bbd9b6d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:25 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 12 Mar 2025 18:47:39 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:47:45 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926fc8d5e8fe4f0ed1123714aae6f738dcd1994fdcc5dcd930aaca6be26db373`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7635d634a216505c60d3666099eb0d5afd323705306c83730f84b9bf84e0712`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c5657a5ff0e793eb645db2765acd1834ebe210c1b31872e58cdf5277eb6909`  
		Last Modified: Wed, 12 Mar 2025 18:47:55 GMT  
		Size: 72.8 MB (72778132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:160dd7a3a7b44acbf4ced9dcc384c34c00c90bee8fe9c1c28440a887e929d41f`  
		Last Modified: Wed, 12 Mar 2025 18:47:49 GMT  
		Size: 380.9 KB (380923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
