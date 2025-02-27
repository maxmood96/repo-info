## `eclipse-temurin:8u442-b06-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:2029c7df8e42399ac45f733fbe73f55c9c5ca21305276c87a2ec0ea8ebfe8001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:8u442-b06-jdk-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull eclipse-temurin@sha256:d0007688d72355567717bf31b835a92bc1878ff20448ffd735301525d89fbc93
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2455587903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883568a9124179129e52b2405f2725e8eacedbc48177fed9965309f23eb7431e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:38:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:38:06 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 00:38:29 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:38:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936dfd0a2b39b2ca03368de30700c8e06d992ad7b0775dc49e31826cdafb5092`  
		Last Modified: Thu, 13 Feb 2025 00:38:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c41f464c8a64fe2be09d530ce180f0ecd3c8d63192c3a92a673cd4e4ee847e4f`  
		Last Modified: Thu, 13 Feb 2025 00:38:39 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9d10eda2baf1d143cfe5521ecb9e3235839acff2413eab13938880e564aa51`  
		Last Modified: Thu, 13 Feb 2025 00:38:47 GMT  
		Size: 191.4 MB (191369896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b9f89264addca5be30ff0c841a71ac7e697923a68cc56fd9ab9c424be388dd`  
		Last Modified: Thu, 13 Feb 2025 00:38:39 GMT  
		Size: 357.4 KB (357433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:8u442-b06-jdk-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:210d69d391f8591a28a64d71bf693c0969f1fb7fe412c305e46a95ce28f54305
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2328628085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323f330b536d76350b0be4ffa0c4870899104518aa040cd81dc9222070a663e4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:32:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:32:48 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 13 Feb 2025 00:33:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:33:41 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d479c990a2b39bb0c7e3d5abf9860278a13d6bd72c7f8371d9726830b8b472`  
		Last Modified: Thu, 13 Feb 2025 00:33:45 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f95890b0373c661a48abfa34c5bc783996feb4f732815ff39dbdebba6f51b8`  
		Last Modified: Thu, 13 Feb 2025 00:33:45 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7eefaf11968dcc5e8d6d3714807cd50453e0aa6688251e656c49e3cc6419044`  
		Last Modified: Thu, 13 Feb 2025 00:33:54 GMT  
		Size: 191.4 MB (191373228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d503b1e660dbf070f5e744eb856c7ecb1008befd40bbdf825f9c1fbbbfbeb33a`  
		Last Modified: Thu, 13 Feb 2025 00:33:46 GMT  
		Size: 343.5 KB (343460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
