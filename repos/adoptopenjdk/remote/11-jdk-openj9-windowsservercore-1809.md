## `adoptopenjdk:11-jdk-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:2b54b2e45333e16bae66c9830576d012a9d3a59f6c55281af206283f40a45220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:11-jdk-openj9-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:b407f3bc654ca0a1ea64c0e9bd49e721c74ec607c5846a082db0541dafc6c5ad
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2714627561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b647729163509b3917ebe9ff703a25a0f639ef8c348e2dd7366bdac383f4d388`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 17:18:14 GMT
ENV JAVA_VERSION=jdk-11.0.8+10_openj9-0.21.0
# Wed, 12 Aug 2020 17:20:43 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10_openj9-0.21.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.8_10_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10_openj9-0.21.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.8_10_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (7250326e5fad877da447bc1e37dfbfcaca18b10f1acc82ffc557a9421dc068bf) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7250326e5fad877da447bc1e37dfbfcaca18b10f1acc82ffc557a9421dc068bf') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 17:20:44 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 12 Aug 2020 17:20:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd2318982276ef115602fbde07a3983b77a73f2d6fa333d5820952279ae8971`  
		Last Modified: Wed, 12 Aug 2020 18:08:16 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0285784e9fde0a15281c14d0b846dc91b0a6214dbdf0dcc1022bc023c2a67b76`  
		Last Modified: Wed, 12 Aug 2020 18:08:51 GMT  
		Size: 378.8 MB (378756039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e934501a1c07c8aa6c49709fa0e47e0c14b376d83b00ec0226e0c7295957b01`  
		Last Modified: Wed, 12 Aug 2020 18:08:17 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9859d911582ad811e42ed81c4a5a511daf84fc0ea26886ac96bedf8aa279327`  
		Last Modified: Wed, 12 Aug 2020 18:08:16 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
