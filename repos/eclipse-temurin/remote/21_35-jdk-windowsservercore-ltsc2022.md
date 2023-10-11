## `eclipse-temurin:21_35-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:5fe44f7dc4f905c9adfcfcfda103872f3dbdd8330a039fa271a4576d51be43b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `eclipse-temurin:21_35-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull eclipse-temurin@sha256:3de97ee01f2528380175ae277736ae10216a4fe737dc74621f2b3b613904fa3f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2238727238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6f8526c83ebb7e284a0e1c50d23c931f31bdf8f43019415a0f5374b5dd04b01`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 17:33:14 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 17:34:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_windows_hotspot_21_35.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_windows_hotspot_21_35.msi ;     Write-Host ('Verifying sha256 (420b09998ae215154b6665c4d8167a74fd99eb3d4d85d5657ba317666e65e301) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '420b09998ae215154b6665c4d8167a74fd99eb3d4d85d5657ba317666e65e301') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 11 Oct 2023 17:34:35 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 11 Oct 2023 17:34:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e75fd06c305b130cd43db7daa07edec8ba83ad9b9012fcd6d6dd88a717f4f1e2`  
		Last Modified: Wed, 11 Oct 2023 17:46:50 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e206d54db96cb221da1ef6862e26634a37ce36c9efc2b79f6dcab6b613da076`  
		Last Modified: Wed, 11 Oct 2023 17:47:20 GMT  
		Size: 378.6 MB (378615236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d54640091f667505a0f46d63608fe30554a6641d0bf8a554ec0a056a3559419`  
		Last Modified: Wed, 11 Oct 2023 17:46:50 GMT  
		Size: 264.8 KB (264827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad60671bf34a738200de8432b666719b9c774f9a09b1410bdfe342ef6d2191d2`  
		Last Modified: Wed, 11 Oct 2023 17:46:50 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
