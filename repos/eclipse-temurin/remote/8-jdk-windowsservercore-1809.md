## `eclipse-temurin:8-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:32b4c1d08c7822ed8667b160fa18343533ed1cbf33c7b2f5070e475828e4df48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `eclipse-temurin:8-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull eclipse-temurin@sha256:1bd07b6be36e68c2cb660d387fb989ad3b93c8051ad45cd549a9ce37444dd601
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313903611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:075331b93e71dc32ea19de6237a3e9f4a29e5edb605bc0ebc5382d74cd2ba02c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 31 Jan 2025 01:29:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 31 Jan 2025 01:29:34 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Fri, 31 Jan 2025 01:31:41 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 31 Jan 2025 01:31:51 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3c0eba6a6aa17e79e3b46d76551a81caa76ddea4c521bb137dbc71941746b7`  
		Last Modified: Fri, 31 Jan 2025 01:31:55 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f6208417e0064eac718937ddaade0fe8702e784d11c849907ef9a6c5f1fd87`  
		Last Modified: Fri, 31 Jan 2025 01:31:55 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419584a376dde4b53063ee975c266b5f899f21ed9d5afe64425fa84b824a61f3`  
		Last Modified: Fri, 31 Jan 2025 01:32:04 GMT  
		Size: 191.4 MB (191375021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6431c232e4459898eda409fbee4b3ae6c155e2feb727069a89c62bdc310ab8d`  
		Last Modified: Fri, 31 Jan 2025 01:31:55 GMT  
		Size: 313.8 KB (313781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
