## `eclipse-temurin:21-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:2d71fde27ac4f7d46076bc073cbca165690cf90ad6ca18e104b7c20c528010f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `eclipse-temurin:21-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:8521b9158a3218914470fed452a3c96b24f54b749b410ace6cc4dd26bcbc91e7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2291463429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c0dc73bce9f140f3776f2982d2e5e29c999ce47523ffefe1c4f8040321a241`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:09:31 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 14 Feb 2024 20:10:35 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_windows_hotspot_21.0.2_13.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_windows_hotspot_21.0.2_13.msi ;     Write-Host ('Verifying sha256 (d0c53b1bfa741b7f6484200faf8452e5a779357c2a29aa6b0dfdedf7173e903f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd0c53b1bfa741b7f6484200faf8452e5a779357c2a29aa6b0dfdedf7173e903f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 20:10:58 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Feb 2024 20:10:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59801d1b9e096dd6dd0078036b1fdadf55d26b97df4b14007a093ca3c28d5508`  
		Last Modified: Thu, 15 Feb 2024 00:13:41 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d1a3f75994dffcbaca6f55149a698d7baa1383683cf289257c75fdc75a5dbc1`  
		Last Modified: Thu, 15 Feb 2024 00:14:09 GMT  
		Size: 380.5 MB (380526370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1286cada0a6520bab6f721184f9b99f548a4e9946a225d1e7b197857a8099712`  
		Last Modified: Thu, 15 Feb 2024 00:13:41 GMT  
		Size: 278.7 KB (278652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea790eda33d6d86d867123a40d2c556a037e62e18c1db50bdf6535b119cbdf71`  
		Last Modified: Thu, 15 Feb 2024 00:13:41 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
