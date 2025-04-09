## `eclipse-temurin:8u442-b06-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:bf0c406ee692b12c038e8d31d10bafd699f47f4f0736ab5a7419a5f6f9c6e91d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `eclipse-temurin:8u442-b06-jdk-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull eclipse-temurin@sha256:3309cf53ed727e738914234f068cad3ad662c011ff0a118a7ad067e587e1a2b6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2354425442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a9ec0bd98edf5b4472fb537b5a419e4126bb72204bcc5715b69a8f66966edda`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:45:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:45:09 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Wed, 09 Apr 2025 00:46:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jdk_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fac13d03d3d193509d82ef964060c21f2b20bc0ca3419ecc5cb3ef71283f2f94') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Apr 2025 00:46:22 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7cc1e7994bf0ca5dd9a9b0bd945fba81369aa13637cba2a041f7af6141ea0`  
		Last Modified: Wed, 09 Apr 2025 00:46:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427215da73c12b0a6c69ba6c66c451bd2ff6b7241b4bd6a1cf0d4738aa6b2a97`  
		Last Modified: Wed, 09 Apr 2025 00:46:25 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b980b1864f02159e15ab0069adfe828cd1c5ce57cecd4c3b6c8443a99812f1`  
		Last Modified: Wed, 09 Apr 2025 00:46:33 GMT  
		Size: 191.4 MB (191364898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ffabd1cc76f6182612c9bbd8ddb7b7eb56d1bfac53d12a4d0f8daea880aaacd`  
		Last Modified: Wed, 09 Apr 2025 00:46:25 GMT  
		Size: 332.1 KB (332113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
