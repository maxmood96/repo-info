## `eclipse-temurin:21-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:db86723394c09a38232e2b4fe1c1d0d026b711b5900153668d9a05e486b5ec79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:21-windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:405a7db5e5342458f89d9cef3aadcf285f353c000e1f78bfe61b17ca9e27baca
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2661324763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e81ec252d6cb06481abd7bd49b2857894f4fc136def0030144426442f0657f5b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:06:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:06:53 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Jul 2025 18:07:16 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_windows_hotspot_21.0.7_6.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.7%2B6/OpenJDK21U-jdk_x64_windows_hotspot_21.0.7_6.msi ;     Write-Host ('Verifying sha256 (168e3c710448dbdd7e6fe2463b867339a72be11a7c8615d72d19fb26572d3619) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '168e3c710448dbdd7e6fe2463b867339a72be11a7c8615d72d19fb26572d3619') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:07:24 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:07:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:439c7abe4d8e32ff459025673c7011b53e375715f0adb0be7a2f249a0af4f9f7`  
		Last Modified: Wed, 09 Jul 2025 19:08:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:794167e073a5f4346aa58c47f9b614b3692d52aadb07ce8cac83c71e3da0a5db`  
		Last Modified: Wed, 09 Jul 2025 19:08:16 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32e7a5bdf717771bb1fb94ec0c37f3d7776c812ca26a7cd46e80e5f1f0f7e7c2`  
		Last Modified: Wed, 09 Jul 2025 19:08:57 GMT  
		Size: 380.4 MB (380369439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b359d87f3122251c440b9e9812b4b8ddd686dc3991dad052988de369aa9256`  
		Last Modified: Wed, 09 Jul 2025 19:08:17 GMT  
		Size: 348.0 KB (347997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a398a49684984c88640320ad7b2a101466857a6dbd954c737bf3f86ebc710a4`  
		Last Modified: Wed, 09 Jul 2025 19:08:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
