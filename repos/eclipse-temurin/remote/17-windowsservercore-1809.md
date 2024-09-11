## `eclipse-temurin:17-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:c3778e30d8490bca0b5ed6a7f58b7f3cd17c728dab87495a58634e2c73023dd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:17-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:bb535973015b9b9c114731422154541201eff81d6b6e27c4e2d37500108273b3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2077641527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:287e0f0d31c6ddade6918be75f2a5b371271a98eef86c3b895eb22b94680f6eb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:48:56 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 11 Sep 2024 00:49:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jdk_x64_windows_hotspot_17.0.12_7.msi ;     Write-Host ('Verifying sha256 (1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1e6df6b445d9e995e86fd8225c658df1411d3abab86b540ce4d2063c8a889835') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Sep 2024 00:50:08 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:50:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b681a22e2ab818abdc55dff7075266cbdad9e0c1d79f16a962cabde9559b4bc1`  
		Last Modified: Wed, 11 Sep 2024 01:17:09 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef860dcb69bd28ef1df6223bc3683386e5dea91d233d1cac40497c31979de6e`  
		Last Modified: Wed, 11 Sep 2024 01:25:53 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d7eb4ecc7b3599bad7c3396f1dce55b9a02820e09661967fd267959aae556df`  
		Last Modified: Wed, 11 Sep 2024 01:26:17 GMT  
		Size: 353.6 MB (353581062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab5b2479974752bb94284cdb417ac7ce5edd91ab79997f5bb8bb851437a17a5`  
		Last Modified: Wed, 11 Sep 2024 01:25:54 GMT  
		Size: 3.8 MB (3787899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e90f987f2e8a5438209af5af5d913df7c7b76897e0cbe0db19989f11ae6281`  
		Last Modified: Wed, 11 Sep 2024 01:25:53 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
