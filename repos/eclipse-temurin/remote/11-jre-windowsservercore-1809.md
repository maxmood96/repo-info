## `eclipse-temurin:11-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:beaab6c7339f00fa71429669891dbb80a2c6de6a6d62a13fb42d417270ac6f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `eclipse-temurin:11-jre-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull eclipse-temurin@sha256:294c7f5ffadda3523424232a3df2df9655a9605a536045515a74437e8ef3efd8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2090428037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bafae1614bd1eaa22ccd47283d48482e0d928c1031e32d08468c2d0b0038b1c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:37:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:37:02 GMT
ENV JAVA_VERSION=jdk-11.0.25+9
# Wed, 11 Dec 2024 20:38:05 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.25%2B9/OpenJDK11U-jre_x64_windows_hotspot_11.0.25_9.msi ;     Write-Host ('Verifying sha256 (577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '577f448ffe2737633bdc2a02e5c53ecccaf3317274b7013b6eb25e9de1934a79') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Dec 2024 20:38:12 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafc65fd2306e5ae2e617da25c28ef3b1743778faba2b9e13dd4d76ce51344ae`  
		Last Modified: Wed, 11 Dec 2024 20:38:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ba13610bcf3369d1d9847d98122d794940826a1d428c24535e7d1f201926e6`  
		Last Modified: Wed, 11 Dec 2024 20:38:15 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f072b7a37b41967221be7138a77e607842a2978e49f5988ff8679a5dbc67d016`  
		Size: 75.9 MB (75918820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda77eac968d553ce11c1fe84df044a2ea1df9b8a2fe815e97d23f6507496096`  
		Last Modified: Wed, 11 Dec 2024 20:38:15 GMT  
		Size: 336.4 KB (336439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
