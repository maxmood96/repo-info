## `eclipse-temurin:22-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:ed9c8acb9a644dfad5b8b21543ac86bfdf16a5602604b03f91c425370c7736b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:22-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:8aabdd2c4adb3d761633417ddbc4255b7618b08afdfbd6bb4b4b491071061b28
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2379623620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc46dc49dea873cefc7d459b51731f6f33790b45c5e330efca386350e514c391`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 00:23:20 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 10 Apr 2024 00:24:25 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_windows_hotspot_22_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jdk_x64_windows_hotspot_22_36.msi ;     Write-Host ('Verifying sha256 (a825f7098a99a6e6a6dca621ba58a60ec285eee19a27e641870ff7cdfd223a85) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a825f7098a99a6e6a6dca621ba58a60ec285eee19a27e641870ff7cdfd223a85') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Apr 2024 00:24:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:24:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8f09cbd064301fb6b1662d3b8e54726a3398664f396c9becfc2fe65cc6b22`  
		Last Modified: Wed, 10 Apr 2024 00:57:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb10df4cb79c37e72f17141196f78fc2af87ff92b48025d4d5db350704fe494`  
		Last Modified: Wed, 10 Apr 2024 00:57:42 GMT  
		Size: 380.0 MB (379978927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a92ab7e02dffa1dd3b02e5533631dbeca8f002c72facd8ea3ee6a74c34739e`  
		Last Modified: Wed, 10 Apr 2024 00:57:15 GMT  
		Size: 266.8 KB (266829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b83a2308821f8d252b433455227f7efbc58d33563ce626a49a476e7c03287caf`  
		Last Modified: Wed, 10 Apr 2024 00:57:14 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
