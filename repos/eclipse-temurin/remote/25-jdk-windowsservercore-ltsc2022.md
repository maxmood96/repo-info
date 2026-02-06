## `eclipse-temurin:25-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3d7aefc693f5b2c88ad08457fb7f96f417fa3e324e112153dbd4050d5853f106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:25-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:63bddf30849788d0b542c90a8518770e44cc14d3b83892358f32f9b35329468e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2089702969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:824866fde69f2390bc97c16d94651f6f2572da65de532d77a12fc617e28d293d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Thu, 05 Feb 2026 22:15:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Feb 2026 22:24:07 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:24:52 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin25-binaries/releases/download/jdk-25.0.2%2B10/OpenJDK25U-jdk_x64_windows_hotspot_25.0.2_10.msi ;     Write-Host ('Verifying sha256 (c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c433b59ab42630634657ae273940183c2f95a115dd5bf6846a70dcd0a42b9c0d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-25' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 05 Feb 2026 22:25:06 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 05 Feb 2026 22:25:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21173afceaa1d09b3f3f4b9c1c2664db824e745b9cacafb8be63e9c677fdfa78`  
		Last Modified: Thu, 05 Feb 2026 22:16:57 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5942296515731eb0990772a9684f0bb009efb248c880632d906618b4a349bb0`  
		Last Modified: Thu, 05 Feb 2026 22:25:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99764f9d8cc0fe1569ba0d112ef018df65a19c2f0f402ce4cdedad245a070485`  
		Last Modified: Thu, 05 Feb 2026 22:25:26 GMT  
		Size: 253.7 MB (253672854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc96e6d10a993395f589ce2699ee7833bf9af7427119142219b2ca0eb6ce2915`  
		Last Modified: Thu, 05 Feb 2026 22:25:10 GMT  
		Size: 367.1 KB (367056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd92582ab33c83cdc87e6cf0a76fc31368841488191d038eb38aa487ef438eb`  
		Last Modified: Thu, 05 Feb 2026 22:25:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
