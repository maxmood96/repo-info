## `eclipse-temurin:8u462-b08-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:72b82d6b624da50eef528bfa918f36336a876acacb779ff09506e28c550d4686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `eclipse-temurin:8u462-b08-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull eclipse-temurin@sha256:aab8acf1cc37261b6c0ff822284892db43eefd6a0163a176501b4e8d3018f2a6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1680639006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0449d3e5317aa9d20e92dca369074bfc35221d92545d742a29f72ded5ac37e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:46:47 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Tue, 14 Oct 2025 20:47:04 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jdk_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (6abb1058eb80b3ae13f63cd7aef302724aebaf0a68924fee6a503ff4a0a39901) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6abb1058eb80b3ae13f63cd7aef302724aebaf0a68924fee6a503ff4a0a39901') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Tue, 14 Oct 2025 20:47:10 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac -version'; javac -version;     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c73b68129a17f163f24c548f99fac1fa06db5f2df83addedaeeccc104c116fd`  
		Last Modified: Tue, 14 Oct 2025 20:46:39 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2209bc82a806f9bc5ebbef28aae43f4aacd827ed5a0f39c7414b519376a0d1`  
		Last Modified: Tue, 14 Oct 2025 20:47:33 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4632cfd641f223c86352f3072ae49864dcbfcb6e1f64c4f8a1e5cbee9c2dda6`  
		Last Modified: Tue, 14 Oct 2025 21:16:01 GMT  
		Size: 191.3 MB (191264456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaef6fced8f780d2a98ab735418232f30e9208e1a16dc4edfdbeeef6d1bce6b2`  
		Last Modified: Tue, 14 Oct 2025 20:47:33 GMT  
		Size: 352.8 KB (352828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
