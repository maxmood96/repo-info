## `eclipse-temurin:17-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:3c8af703a236f89e247354a59d5399ae62e58bcad005d85708550a821e45731f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `eclipse-temurin:17-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:edecb7ce2655a15fea2643f2aa4b98c0fb63520951a7446e285450c3a91e3275
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2473639361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76aadcbb74ec8177963dd3e0b143327c8b8cb99f4b9ea22fa5795d836cf5d6b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 17:36:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 17:56:13 GMT
ENV JAVA_VERSION=jdk-17.0.11+9
# Wed, 12 Jun 2024 17:57:13 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.11%2B9/OpenJDK17U-jdk_x64_windows_hotspot_17.0.11_9.msi ;     Write-Host ('Verifying sha256 (99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '99ad599eea572207026f2b85159ef4ec06c620cee88662ea108f0013697b0365') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Jun 2024 17:57:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 12 Jun 2024 17:57:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045fa3135d89819dc64e63c6fd4e832a9b86fc2d37e11e64d811218c4a684924`  
		Last Modified: Wed, 12 Jun 2024 18:36:56 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00f493482b99143f5c19a79d27a64bb5248e036a32da37e5726d54cb64dcae9`  
		Last Modified: Wed, 12 Jun 2024 18:44:44 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91fe62fb22399fdf32769785c77db9c5687395387fe2a40553c418029fbd70c9`  
		Last Modified: Wed, 12 Jun 2024 18:45:10 GMT  
		Size: 355.2 MB (355176090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965c1f6d94abe7dd75bd35439134d7449872bceda82c55264ccf89c6186989f3`  
		Last Modified: Wed, 12 Jun 2024 18:44:45 GMT  
		Size: 280.3 KB (280271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d244c49aff0a3608cb00056fbcdfcebe830a444ed2c8ba704f86232a5d5dbb61`  
		Last Modified: Wed, 12 Jun 2024 18:44:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
