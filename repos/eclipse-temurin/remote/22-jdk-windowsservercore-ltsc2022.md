## `eclipse-temurin:22-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:d68241d1acc89145d856e796ff52f83662b86c57a5d999483fdc7af44e76cc29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `eclipse-temurin:22-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull eclipse-temurin@sha256:be4111b3e03c33dc73bd6175fdc6daa235fb793fb188b38b4e194fa8055001d8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2379699330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5297f0d83c4b81b2a00519e6018667d93ec8df5d69c64d5cdd6c7428357a7ef6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:37:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Apr 2024 19:11:10 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 24 Apr 2024 19:12:12 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_windows_hotspot_22.0.1_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin22-binaries/releases/download/jdk-22.0.1%2B8/OpenJDK22U-jdk_x64_windows_hotspot_22.0.1_8.msi ;     Write-Host ('Verifying sha256 (89387f079e372b70a57c6a2f778a4020144cb19ae44f49b066c83d9410938e2f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '89387f079e372b70a57c6a2f778a4020144cb19ae44f49b066c83d9410938e2f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-22' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 24 Apr 2024 19:12:34 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 24 Apr 2024 19:12:35 GMT
CMD ["jshell"]
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
	-	`sha256:69d3551a4909976fc10ecaf9464d66f8e70f1caba50a68067dd3b27998a0ba6a`  
		Last Modified: Wed, 24 Apr 2024 19:43:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6d75052f5e4c9d249329cd8935f1171d85610198dff8cfefe356378a4e44bc`  
		Last Modified: Wed, 24 Apr 2024 19:43:38 GMT  
		Size: 380.0 MB (380031867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5687d4f377cc21e62941b6f7cffe883e08ca33daad6d819073c25f7aed15673e`  
		Last Modified: Wed, 24 Apr 2024 19:43:09 GMT  
		Size: 289.7 KB (289704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6293af2f0dc10ac78193ab844172f111626977b268f074c95b8cb68a9383e898`  
		Last Modified: Wed, 24 Apr 2024 19:43:09 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
