## `eclipse-temurin:11-jre-windowsservercore-ltsc2016`

```console
$ docker pull eclipse-temurin@sha256:cff2938c8eb0c4cd856c63b720f31320a89343fa25a391e19d7cad8375d47677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4651; amd64

### `eclipse-temurin:11-jre-windowsservercore-ltsc2016` - windows version 10.0.14393.4651; amd64

```console
$ docker pull eclipse-temurin@sha256:6ed8f940aa263cbce4e6cf77af7dff3843fd2ae9cc493b92eb2273ea5fdbf5c8
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 GB (6345086208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26b646f506cad7c920f0786e3cb76abbf3c3c4da01bba8d3d5d92a178eb11360`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 13 Sep 2021 01:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Sep 2021 00:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 16:28:20 GMT
ENV JAVA_VERSION=jdk-11.0.12+7
# Thu, 16 Sep 2021 19:20:40 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.12_7.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12 ; Invoke-WebRequest -Uri https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.12%2B7/OpenJDK11U-jre_x64_windows_hotspot_11.0.12_7.msi -O 'openjdk.msi' ;     Write-Host ('Verifying sha256 (665c22ab930ffa8a220c92b0c08f3cc993c864d7d0ddd8971ab2d738cc03db46) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '665c22ab930ffa8a220c92b0c08f3cc993c864d7d0ddd8971ab2d738cc03db46') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 16 Sep 2021 19:21:40 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9b8281bf21e46c781fb54e4f15f5728e2c44dea4219c9e6deeb732f1d909d3b`  
		Size: 2.2 GB (2201342322 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8721f004192f15fe71b8626ef3f3e34cbf2cfe1d15a63b6b544ab946162ef707`  
		Last Modified: Wed, 15 Sep 2021 01:10:18 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bad1262ba6d2ce354dd77660b54caba20d1b11cc7f16b064df1ea6fb2716467`  
		Last Modified: Wed, 15 Sep 2021 16:51:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1051bb2694cdaa454d135ab401ba52e61eae7159ba65bb31c89c219a2620f0`  
		Last Modified: Thu, 16 Sep 2021 19:25:40 GMT  
		Size: 73.5 MB (73450492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7e81faed5f97407b21f9fabc1f54b7a7cf5ee3f11dece628f66376201991d8`  
		Last Modified: Thu, 16 Sep 2021 19:24:23 GMT  
		Size: 304.9 KB (304887 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
