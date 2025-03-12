## `eclipse-temurin:21-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:1fff9e002d3d696bb17002948daba4746dd3a2c8b67c8881bd2b7f4ae4ae3f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3476; amd64

### `eclipse-temurin:21-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:9adffe3cf059cfca5850aa8b6792a60f0cbe07b2bd653929615cf8d363e8e013
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2992609415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2506abb8e48cc3ced371b7f7aa70ff6d22c70e0e25de2890f1fc16efe7da3e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:47:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:47:56 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 18:48:11 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (3f511d4edbb81fdb7d044cabede018b0823b2f277103f5f47e8c72b526e9c256) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3f511d4edbb81fdb7d044cabede018b0823b2f277103f5f47e8c72b526e9c256') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Mar 2025 18:48:17 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a80c2ffbf1c8e10164525bade21c88ad3524e3ce67f2d68147ad3148c0f825`  
		Last Modified: Wed, 12 Mar 2025 18:48:20 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:644f4d3bad12b3ff1e127cef2183192fef7f17425639270447bb0a52c85fbf5a`  
		Last Modified: Wed, 12 Mar 2025 18:48:20 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff718a971e6ba4889a2918642a02b775d269f78afcf8e683be5b68a55b3a79bb`  
		Last Modified: Wed, 12 Mar 2025 18:48:27 GMT  
		Size: 83.6 MB (83580085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6c241b517249f6b5521a7794ff157934a23f9c6ac7d01b983262b3b25deec35`  
		Last Modified: Wed, 12 Mar 2025 18:48:20 GMT  
		Size: 379.0 KB (378983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
