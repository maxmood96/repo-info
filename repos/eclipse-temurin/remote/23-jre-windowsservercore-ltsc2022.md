## `eclipse-temurin:23-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:8954b6acd09d97c4dcc1869da58b62a4748d7040132891d462d0af9059b0f289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:23-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:cd56d3c703f5cb46051c34a80dc7f944fefec6abbc66aefb6294584123178bd7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1883920228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9311583e1b279cf23ae929c929643a198358c73af1ddcd8218397eba8207e97d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:33:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Oct 2024 00:04:36 GMT
ENV JAVA_VERSION=jdk-23+37
# Thu, 10 Oct 2024 00:09:08 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jre_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '90877250f1f0195cdb241f5c75068e70383d25895567416cde0201abf33efd3c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Oct 2024 00:09:34 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd7a167e5d8024c2db3283a385811103c47c1e1349528ae29d41d1aa3117ae`  
		Last Modified: Thu, 10 Oct 2024 00:18:53 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b382d6d68061f3371be6f50b9b98bf213d56f8a3d84748b96d1d8aedb166a5d`  
		Last Modified: Thu, 10 Oct 2024 00:30:48 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aef43083ee1e4a5939751cf7b3d4adc773d8a823d14d6bb9426335411d02b2d`  
		Last Modified: Thu, 10 Oct 2024 00:32:18 GMT  
		Size: 84.3 MB (84289593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:019529abf8d62745b83ef0ff9ad7b93e6f87043df0078e49adfb9fab478c00ee`  
		Last Modified: Thu, 10 Oct 2024 00:32:07 GMT  
		Size: 286.2 KB (286249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
