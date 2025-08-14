## `eclipse-temurin:21-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:00cccbfce48e3425402bfc69720e2de0b8419570da0427d6b1937a7fdaf24150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull eclipse-temurin@sha256:d223c9b15472edce69c81ac8dbaa6b2843ab7455712ab48aed9218333f4473a2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3582770468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb0ae85388b6955eb4e3b60693690b55a5a7d7bc9cae432c4d831a8e5cd2697`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:45 GMT
ENV JAVA_VERSION=jdk-21.0.8+9
# Tue, 12 Aug 2025 20:28:00 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.8_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.8%2B9/OpenJDK21U-jre_x64_windows_hotspot_21.0.8_9.msi ;     Write-Host ('Verifying sha256 (9e38a94eed115fb834c2c4375bc493cef1a47e28c82bd83f623efe3fca017e7a) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9e38a94eed115fb834c2c4375bc493cef1a47e28c82bd83f623efe3fca017e7a') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 12 Aug 2025 20:28:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e79cf9866396fb63a2141bb52e7bbccf4cbe7195269989ec1953c4f29bfbd95`  
		Last Modified: Tue, 12 Aug 2025 20:32:07 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b806d09e43fac17965aae3e473f2447c0c78d047d3831840a7af389982d41a48`  
		Last Modified: Tue, 12 Aug 2025 20:32:06 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d673e2fb4fe56deb004ca0a42ffb774806548cdfffbd24d7d20291651074e1b6`  
		Last Modified: Tue, 12 Aug 2025 20:32:14 GMT  
		Size: 83.6 MB (83570950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888cb571a8206caf27af14c412345b3aeb56da7ba639101c626fdc4a2e4e6ad9`  
		Last Modified: Tue, 12 Aug 2025 20:32:09 GMT  
		Size: 366.4 KB (366440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
