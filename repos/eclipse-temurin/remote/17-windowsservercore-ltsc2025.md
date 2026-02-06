## `eclipse-temurin:17-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:bd8a214204ee06c228a9d41ef6a4c16cd9c360d779c5b860ce0923e980c2cf52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:17-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:2b778d15f9e48c13b631c7d4842d7bfca5dedea905c8c0eaca603f821003104b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1851713752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b23f3a676c7e7f5d77e482be8cdabd7e2b5172b5cb631afafd05d89beb69b35d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:16:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:16:39 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Thu, 05 Feb 2026 22:17:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.18_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.18%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.18_8.msi ;     Write-Host ('Verifying sha256 (bd169b6b8439e1d715eff789e355029e222ce6152994cefc3e666783ade8ff44) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bd169b6b8439e1d715eff789e355029e222ce6152994cefc3e666783ade8ff44') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:17:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 05 Feb 2026 22:17:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5198aa9a71279b3066342867e905cd646c0a02bf5dabb1ba22d914aa022d2081`  
		Last Modified: Thu, 05 Feb 2026 22:17:45 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e7c1d31ad53d702dd799d8a19e26b2b7640ad002b4c872dd7c385c141b82c8`  
		Last Modified: Thu, 05 Feb 2026 22:17:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1f78448ca65d6bcd2e5651c11a51d1721223747423e1635cc8803ed54576f7`  
		Last Modified: Thu, 05 Feb 2026 22:18:04 GMT  
		Size: 355.6 MB (355550043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:907e0b0b8c73c035698b947c490ad7bed1b843bd31f269714de5eec7c74a2c2c`  
		Last Modified: Thu, 05 Feb 2026 22:17:45 GMT  
		Size: 399.5 KB (399524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbccf8cce583d78192d7152d0f42b6dfbf22985a1ac4662ef656e2b00b9a7c66`  
		Last Modified: Thu, 05 Feb 2026 22:17:45 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
