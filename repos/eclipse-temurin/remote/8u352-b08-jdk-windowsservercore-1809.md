## `eclipse-temurin:8u352-b08-jdk-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:8e2520e3a35306115d0377a5add766923735afd4e1cc93e107ab3eee20bd7a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `eclipse-temurin:8u352-b08-jdk-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull eclipse-temurin@sha256:d22c4050ba35c07cb02f3887813c29267e49a6534dafcde37566f1912cc26e3a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2968435594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464d728ecfd646837ddf7a3ef2e56b3ba2b7a8503471bab351ca03ddb1a893b4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Tue, 08 Nov 2022 18:31:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Nov 2022 18:31:27 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Tue, 08 Nov 2022 18:34:17 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u352b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u352b08.msi ;     Write-Host ('Verifying sha256 (c3f2ee62970bae81aa163e155faab8498638962a0a480aa01620d3122ad902ee) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c3f2ee62970bae81aa163e155faab8498638962a0a480aa01620d3122ad902ee') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 08 Nov 2022 18:36:13 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f182832ad6ad5ea3d4b7320fd7bfea56fb9cf8413be904e52db6ed14c8d9e36f`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e905ec7ac6286120819ee4665abdd5686c4a710b97b682700e742ddef09c72`  
		Last Modified: Tue, 08 Nov 2022 19:42:07 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5eba66ad0d7870d9e91268b72f9670ad546c939baad9b4b7f967c94bc2420fe`  
		Last Modified: Tue, 08 Nov 2022 19:42:36 GMT  
		Size: 189.5 MB (189516164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a806afd090232e4f0838e73b0506d6a80feba893512ad92770f37878431488`  
		Last Modified: Tue, 08 Nov 2022 19:42:08 GMT  
		Size: 329.7 KB (329738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
