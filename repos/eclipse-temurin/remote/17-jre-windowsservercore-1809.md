## `eclipse-temurin:17-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:18c1b3c5b4a02964d420e473fba7a9657c48728613841929811ce68b7ea4c104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `eclipse-temurin:17-jre-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull eclipse-temurin@sha256:78241ad87502d54496d02cd3c3c651cd366d316fcf83cada23dac0b5e934b03e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1797916262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:266b49602a052d0e9a8c78cd9522a86ad535fad8b05a72c493c3ff918c17b654`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:48:56 GMT
ENV JAVA_VERSION=jdk-17.0.12+7
# Wed, 11 Sep 2024 00:52:44 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.12_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.12%2B7/OpenJDK17U-jre_x64_windows_hotspot_17.0.12_7.msi ;     Write-Host ('Verifying sha256 (62caaa23b88545099612ae77455fe2ac888ad3731ac0758f5cbedad406fd3c6c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '62caaa23b88545099612ae77455fe2ac888ad3731ac0758f5cbedad406fd3c6c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Sep 2024 00:53:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
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
	-	`sha256:7df3ab96baf7e37c9643d10fc899c12df3de2ec92e6b20bb7bdf8c2beb225e27`  
		Last Modified: Wed, 11 Sep 2024 01:27:22 GMT  
		Size: 74.5 MB (74450927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c887e3878b5193d1edd9a62ed3ec9c2bc6fc1ea67106165eb1cfe6b3d1eba0b`  
		Last Modified: Wed, 11 Sep 2024 01:27:15 GMT  
		Size: 3.2 MB (3194160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
