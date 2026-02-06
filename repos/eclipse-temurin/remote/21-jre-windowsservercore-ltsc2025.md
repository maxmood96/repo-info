## `eclipse-temurin:21-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:2f6d7c2c6152ee79bf1b461935772371c4a9d449326aabe86e5f7f84ecb84b28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:bb71ce1f084d46264d7a38dfbc92345c501efe9d239acc7ba76b54efee993c6c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1579807293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a2acd2d6fc644ce098d10193c3ae5e186a1c564be6c14c427776adc080e723b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:18:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:18:17 GMT
ENV JAVA_VERSION=jdk-21.0.10+7
# Thu, 05 Feb 2026 22:19:02 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.10%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.10_7.msi ;     Write-Host ('Verifying sha256 (a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a841118d4959b6b6eb6156fa1f2487f112afaecd124b1eb5bba203d5556efd32') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:19:09 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b601f27219bae14205bab18eeffef90c3004cc219b406781f227b617c4d9e96`  
		Last Modified: Thu, 05 Feb 2026 22:19:13 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db8e9290e5571671281ca93c0d0278b55ce92d28e33a7e95472d10ed4e2d0fa`  
		Last Modified: Thu, 05 Feb 2026 22:19:13 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88676e38263396098bd94c62cf8a4b4e16396a1a4c43009e34ca1cbd84de0fa3`  
		Last Modified: Thu, 05 Feb 2026 22:19:22 GMT  
		Size: 83.6 MB (83645339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04da68c497fa91d52031b63b27cf9f61180e943fc4d838d13a3de4524efd9d37`  
		Last Modified: Thu, 05 Feb 2026 22:19:13 GMT  
		Size: 399.0 KB (398992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
