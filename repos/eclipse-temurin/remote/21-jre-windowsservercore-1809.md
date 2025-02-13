## `eclipse-temurin:21-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:4538c065a1aba2f50ac98130ffcc5f542acc87c3cd67ccbb449b72567d03b8c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `eclipse-temurin:21-jre-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull eclipse-temurin@sha256:f184279b4256d38383c33d9eafd309e56a740bca240af2c64d9fd086cfdf1282
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224088325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd22aea5ec79f2292cecaa6ebcf4f4283e2ce56001eb5191f40f1007163c463`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:36:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:36:04 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Thu, 13 Feb 2025 00:36:59 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.6_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.6%2B7/OpenJDK21U-jre_x64_windows_hotspot_21.0.6_7.msi ;     Write-Host ('Verifying sha256 (3f511d4edbb81fdb7d044cabede018b0823b2f277103f5f47e8c72b526e9c256) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '3f511d4edbb81fdb7d044cabede018b0823b2f277103f5f47e8c72b526e9c256') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Feb 2025 00:37:07 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af918f13a02374d5477ecb63e071127ae0ed76b3ee548f9802671f3fd47f60ed`  
		Last Modified: Thu, 13 Feb 2025 01:08:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd7fb0883828d19d70a52ad04c278d4be6ccf9f570aa3d9a70b22a91db6a83d`  
		Last Modified: Thu, 13 Feb 2025 01:08:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6687f29178d784e8a64997b103e8f65c9626274a698bac64f836093cda30830e`  
		Last Modified: Thu, 13 Feb 2025 01:09:13 GMT  
		Size: 83.6 MB (83562527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123b51d432818cd2f8881c00cdb0544ec073bc0b03ec31d969819e87df5e4017`  
		Last Modified: Thu, 13 Feb 2025 01:08:56 GMT  
		Size: 3.6 MB (3614388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
