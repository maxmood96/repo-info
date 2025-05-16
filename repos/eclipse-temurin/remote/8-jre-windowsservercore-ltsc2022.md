## `eclipse-temurin:8-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:dc5730f823f80b073a9cae9563dc9ce38190ae9052bbc2f792fb79041d3d1a73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `eclipse-temurin:8-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull eclipse-temurin@sha256:d43c1caa1993509c4bdff5b47a61165039f67d061a9c7db5bef79016d2515636
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346724858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376eb29fa37e2f2eb5c698474bd5606c870c167072d42a4ec709db89bc59cebd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:53:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:53:36 GMT
ENV JAVA_VERSION=jdk8u452-b09
# Wed, 14 May 2025 20:53:51 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u452-b09/OpenJDK8U-jre_x64_windows_hotspot_8u452b09.msi ;     Write-Host ('Verifying sha256 (aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'aa75823c6dee1d65b53da6b1e9bd7de8a521e01f7e95dea2b5f104be0ee58242') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 May 2025 20:53:58 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68075167d1c2414b602295f62007c8b08851798a67669d43ebd1c682195b2139`  
		Last Modified: Wed, 14 May 2025 20:54:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90fa0b2bc1ad6c5fa2f0ca272f0d26b72540a5cc9bb5b9077330dccd016db97`  
		Last Modified: Wed, 14 May 2025 20:54:02 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93135516aca71f6034c51aa66595099d53c149a6a6a705e24a2a5a005e38d3f3`  
		Last Modified: Wed, 14 May 2025 20:54:07 GMT  
		Size: 72.7 MB (72746831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efc0b3810c63f04e2b64895e1fd8de7979bea434895c485d4696df9b66b3b1d`  
		Last Modified: Wed, 14 May 2025 20:54:02 GMT  
		Size: 347.3 KB (347338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
