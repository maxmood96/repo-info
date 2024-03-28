## `eclipse-temurin:22-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:a33433145a6cecd825f46f5961896eb8d18886d8ff526394cbfacc11271ac9f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `eclipse-temurin:22-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull eclipse-temurin@sha256:0b53ce9e9b03490d4399e542d4a74d3bcb75374f1999f1031e08d3e3a3933a97
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2040915662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1265172e9bc104f123af255a39737cb4bcfebccfe76627374b9a2179199363f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:36:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 28 Mar 2024 01:18:59 GMT
ENV JAVA_VERSION=jdk-22+36
# Thu, 28 Mar 2024 01:26:40 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_windows_hotspot_22_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_windows_hotspot_22_36.msi ;     Write-Host ('Verifying sha256 (fa6b75f1dbd9eca8bfbd955d2a78d4fc8c678127790caf4340ce2991c7b668c9) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fa6b75f1dbd9eca8bfbd955d2a78d4fc8c678127790caf4340ce2991c7b668c9') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 28 Mar 2024 01:27:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d20fbf24d92fe45a4587956553b64d2dab183e65b8555a90ce446ac29b3a69`  
		Last Modified: Wed, 13 Mar 2024 01:27:59 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f902488db9d25a0f1d5891f0a26d6c8a850ec660ed6b76acefc82a48c518f084`  
		Last Modified: Thu, 28 Mar 2024 01:37:28 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2516c277a893770429f9f415f8009ab196e1641856a02752f0eeb06096a08074`  
		Last Modified: Thu, 28 Mar 2024 01:39:28 GMT  
		Size: 83.2 MB (83174550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01044af3c14109b21e03ee039f6bbe4ed2fb4901e223b461391ec192af8c213e`  
		Last Modified: Thu, 28 Mar 2024 01:39:18 GMT  
		Size: 279.3 KB (279335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
