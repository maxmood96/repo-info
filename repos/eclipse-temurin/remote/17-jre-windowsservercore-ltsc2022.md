## `eclipse-temurin:17-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:95c44834a51a50f48f141420e0a13a9b4bcbb337ea995817825b1316022cb9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `eclipse-temurin:17-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull eclipse-temurin@sha256:3d69ffcf2651d95b24f701739503301f00addcac72b39123bd29193668766e59
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1652718955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c7acf82e5028c210118499499975f6b620151647e6041da45cfc3029603235`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:10:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:21:19 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Fri, 24 Oct 2025 18:21:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.16_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jre_x64_windows_hotspot_17.0.16_8.msi ;     Write-Host ('Verifying sha256 (9937d754d7157dcdb7ec70a83a5e6238ce093c71316435b4dd07ae38880980d2) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '9937d754d7157dcdb7ec70a83a5e6238ce093c71316435b4dd07ae38880980d2') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Fri, 24 Oct 2025 18:21:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b98378885855372677fffe8ed8a7b41c35f9d46d0075c0e37dc6cc153fdc4a1d`  
		Last Modified: Fri, 24 Oct 2025 18:21:15 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180497252c56519e38a65a3237a7fd79c946e80d9b45c9b01bc12028d0e1400d`  
		Last Modified: Fri, 24 Oct 2025 18:21:57 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584f714df6926b862b99d882dc9e78c2087bf910e5ab0214e0ee17fd57dd4924`  
		Last Modified: Fri, 24 Oct 2025 18:22:08 GMT  
		Size: 75.2 MB (75171169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eee2d505a854e4a45104b50030e5d578cef200472ddf5058b9b75e1a9e738f1`  
		Last Modified: Fri, 24 Oct 2025 18:21:57 GMT  
		Size: 352.2 KB (352199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
