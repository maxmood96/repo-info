## `adoptopenjdk:8-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:9db4f60fc2d8afbd5af998ae5decb5f7b626c4d7511f27393e69ac93e016ce91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `adoptopenjdk:8-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull adoptopenjdk@sha256:1d140df1e100060699bec6a81bfcc37bc95ab511c41a0beb2dcbb855aa5c8225
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5939797110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ef39b3ec9c6f84ea5eb4d145277e6bc3e0cb618bdb4022752fe29a0482f7d2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 16:27:42 GMT
ENV JAVA_VERSION=jdk8u262-b10
# Wed, 12 Aug 2020 16:30:03 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u262b10.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10/OpenJDK8U-jdk_x64_windows_hotspot_8u262b10.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (251429e9c5ea2d2950aceca10c67e4bf5be3f5f299f2fad4c9757b5ac857cc2c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '251429e9c5ea2d2950aceca10c67e4bf5be3f5f299f2fad4c9757b5ac857cc2c') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:32838d9637dc39d4acee78700b0f93d6c8c9d2db755f12c8009c1b51687d3fbd`  
		Last Modified: Tue, 11 Aug 2020 20:54:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30023d7600c1a5f75be0dc24ec05711ea75eaa2b42455a094e2a467052fe2f1`  
		Last Modified: Wed, 12 Aug 2020 17:46:48 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00fe284819dc218e8733837a2608be97dbf15fad1913448e52852b36b67aa6ff`  
		Last Modified: Wed, 12 Aug 2020 17:47:26 GMT  
		Size: 201.6 MB (201647401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
