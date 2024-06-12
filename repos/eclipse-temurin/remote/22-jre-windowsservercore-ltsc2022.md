## `eclipse-temurin:22-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:6c79f41333f33f794eadaf51504d82d1214ea95fdb884f80e90925246df89916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `eclipse-temurin:22-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:48ba7686ab34099fa18a4ab6b10b60abb66a953367373cadabb89f0b50c28eb2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201521677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a7d53974ea0b29656ff1fcdd5d4445c80a8d583713d470fcc892986570505d5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 17:36:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:16:51 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 12 Jun 2024 18:23:38 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jre_x64_windows_hotspot_22.0.1_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jre_x64_windows_hotspot_22.0.1_8.msi ;     Write-Host ('Verifying sha256 (6d918aa3c1cbad4c70afe9563f057dcf39b3c2dff2ae01e44e1e89f237399d96) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6d918aa3c1cbad4c70afe9563f057dcf39b3c2dff2ae01e44e1e89f237399d96') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Jun 2024 18:23:58 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045fa3135d89819dc64e63c6fd4e832a9b86fc2d37e11e64d811218c4a684924`  
		Last Modified: Wed, 12 Jun 2024 18:36:56 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3365c0d2967330eb2d7dde49b0234a3912a3616f07a70dd6e936dfdb2e8957c9`  
		Last Modified: Wed, 12 Jun 2024 18:50:04 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b260990c4eb4af4f7c78897ad8a6ea77addf57721ace1b746e98df0b5444ed9c`  
		Last Modified: Wed, 12 Jun 2024 18:52:00 GMT  
		Size: 83.1 MB (83062450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f66e37aac8a60f4700a7fcf5a45ee42aaf8b63be06c2a325ad80c638bb50cd2e`  
		Last Modified: Wed, 12 Jun 2024 18:51:49 GMT  
		Size: 277.7 KB (277668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
