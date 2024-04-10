## `eclipse-temurin:22-jre-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d5890c253b706d9daacdd879e26e0c62a492f06d1fe23fca504e95e3b954299e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:22-jre-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:b9c00b29ec50be7aa38d2e2229b1456d9add4fdacc9cfb07075b3138e43c477a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2082839721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9a5533da74b5c0844507bf038e7410109d635193ed673ee497dfdf4dcbc854`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 00:23:20 GMT
ENV JAVA_VERSION=jdk-22+36
# Wed, 10 Apr 2024 00:30:38 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_windows_hotspot_22_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22%2B36/OpenJDK22U-jre_x64_windows_hotspot_22_36.msi ;     Write-Host ('Verifying sha256 (fa6b75f1dbd9eca8bfbd955d2a78d4fc8c678127790caf4340ce2991c7b668c9) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'fa6b75f1dbd9eca8bfbd955d2a78d4fc8c678127790caf4340ce2991c7b668c9') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Apr 2024 00:31:01 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95446b37fecac1159dce92ccce6a16e77fd3b7c7302e5d36492b37a85cc20e5a`  
		Last Modified: Wed, 10 Apr 2024 00:44:18 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb8f09cbd064301fb6b1662d3b8e54726a3398664f396c9becfc2fe65cc6b22`  
		Last Modified: Wed, 10 Apr 2024 00:57:14 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:126b2212240ecd04b8373333f82cef1957c46d6361940301255e619ba019a36f`  
		Last Modified: Wed, 10 Apr 2024 00:59:13 GMT  
		Size: 83.2 MB (83185024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a94597f5f8a6c4c1efb04685c46368c851a74262b8c6e5c30c0a99d5342d58f`  
		Last Modified: Wed, 10 Apr 2024 00:59:02 GMT  
		Size: 278.2 KB (278238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
