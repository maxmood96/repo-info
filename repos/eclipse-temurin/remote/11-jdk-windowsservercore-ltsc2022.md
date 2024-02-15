## `eclipse-temurin:11-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:6b458c63bb79f1ba34efc2250aa351afee2783fe91c9bc85a97cdeb703f7539b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `eclipse-temurin:11-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull eclipse-temurin@sha256:dfe1f40d80e094333a271f0bc861ff56c4876108256314812e40c64e89ea54f7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2280085743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d46f872d96501ba396f3f2331f27fb307d6ee4aa0f7a1d82f202aa8fb52a0085`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 19:47:18 GMT
ENV JAVA_VERSION=jdk-11.0.22+7
# Wed, 14 Feb 2024 19:48:24 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.22_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.22%2B7/OpenJDK11U-jdk_x64_windows_hotspot_11.0.22_7.msi ;     Write-Host ('Verifying sha256 (a628fdaf29923f4cc2dfd3445369a4c1ce9c205bdf219a8ac33f809d489ffb6f) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'a628fdaf29923f4cc2dfd3445369a4c1ce9c205bdf219a8ac33f809d489ffb6f') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-11' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 14 Feb 2024 19:48:50 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 14 Feb 2024 19:48:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37017920e0d3d53c00b84ece22edf197188167cb6ca0b6f23da5a03f641c2a8a`  
		Last Modified: Thu, 15 Feb 2024 00:08:13 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a4cab55ef8ee24eb0f31bf05fbba71822105a679c05dc8112e467ca487b9bb8`  
		Last Modified: Thu, 15 Feb 2024 00:08:41 GMT  
		Size: 369.1 MB (369138976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e78e7fd7840c5af47171b7a95e7c1e9e2f32a32e96c1edc22c71093038f56d`  
		Last Modified: Thu, 15 Feb 2024 00:08:13 GMT  
		Size: 288.3 KB (288337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b80bf2caf4f995e55858952a29400be36df4259b96f5854d853f03cd9fa6386`  
		Last Modified: Thu, 15 Feb 2024 00:08:13 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
