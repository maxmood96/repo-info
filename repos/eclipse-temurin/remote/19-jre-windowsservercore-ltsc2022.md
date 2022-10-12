## `eclipse-temurin:19-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:144b9d9db2df2742dedea6a611263ea644f1dd98f2736c7c1bba89cf10d48520
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1129; amd64

### `eclipse-temurin:19-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.1129; amd64

```console
$ docker pull eclipse-temurin@sha256:2ed1a4165ba52a9ef279c6ad654ecec37ff8f8b23edc7dd159a0488f5539c6e7
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2494553261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea7ca0697a59c54c87ce22872257b195277abc107d233bcac0069877666c47a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:45:15 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 12 Oct 2022 15:50:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jre_x64_windows_hotspot_19_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jre_x64_windows_hotspot_19_36.msi ;     Write-Host ('Verifying sha256 (2fe3e0989b31551b65cd3d276f8435618aad7f4e3f2996a58c3b51f0de4ccf35) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2fe3e0989b31551b65cd3d276f8435618aad7f4e3f2996a58c3b51f0de4ccf35') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Oct 2022 15:51:17 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f463948dc70c49daeabdf3a3ee0bc99618308729bea7a91f4eca188b14b6e9`  
		Last Modified: Wed, 12 Oct 2022 16:09:54 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee90cf3eddebe67e29acbfba97aaff87792852cbc8fc0ca5ee4c88e68a5d8333`  
		Last Modified: Wed, 12 Oct 2022 16:12:01 GMT  
		Size: 77.8 MB (77789226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc4b836b95c162e94105e7461cc712ad11c46c7612e9e72de4cc8783ef2052ed`  
		Last Modified: Wed, 12 Oct 2022 16:11:51 GMT  
		Size: 538.0 KB (537970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
