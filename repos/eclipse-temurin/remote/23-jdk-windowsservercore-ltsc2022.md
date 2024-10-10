## `eclipse-temurin:23-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:c56bd1ea16f7cfb06ccebf98ffb09354f11b39b154217637cd30db96e9de7eca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `eclipse-temurin:23-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:7091351ef5099dd1b85289aa4ab28b37b7c2df2585cb00470a59f9abbec88232
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2197344556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6642097cafe5603b6b6ffeee06c9be341c632b2103ee646184cc6e24ac40bfe3`
-	Default Command: `["jshell"]`
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
# Thu, 10 Oct 2024 00:05:36 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin23-binaries/releases/download/jdk-23%2B37/OpenJDK23U-jdk_x64_windows_hotspot_23_37.msi ;     Write-Host ('Verifying sha256 (39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '39b7594580597ab85b3b4769d945e70d1665b3b8167c70039db407d2fb36803f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-23' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Oct 2024 00:05:59 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 10 Oct 2024 00:06:00 GMT
CMD ["jshell"]
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
	-	`sha256:4aa5962a6ee97cb71e6b190c38268166a54e657a332a64c77c9481a0827b8063`  
		Last Modified: Thu, 10 Oct 2024 00:31:16 GMT  
		Size: 397.7 MB (397711216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dfcc433e08fc021b50ac6e01e08408460349ce1d42113d68d2636aa445dcfb1`  
		Last Modified: Thu, 10 Oct 2024 00:30:49 GMT  
		Size: 287.6 KB (287578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ae14abf3c3d4938bd1b477728a648b373d15bc6cc1205cafb0b476fb6677de`  
		Last Modified: Thu, 10 Oct 2024 00:30:48 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
