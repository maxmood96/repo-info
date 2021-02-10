## `adoptopenjdk:11-jdk-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:f647c7a5fa5a91e6fc5b2391106b8255ebbc6b54df91e5cb89a3dac8be9b7119
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4225; amd64

### `adoptopenjdk:11-jdk-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.4225; amd64

```console
$ docker pull adoptopenjdk@sha256:f850593ff954d0ee0879138c17098c8ac42b3b9f3f6e0e8e40819ff88098dd51
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6168854694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690a09eb0568b4ff5540dfaab6d0e1f9072485fe9823b0738e2ad12ba25b93bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Jan 2021 18:11:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Feb 2021 13:17:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 17:58:26 GMT
ENV JAVA_VERSION=jdk-11.0.10+9
# Wed, 10 Feb 2021 18:00:31 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.10_9.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.10%2B9/OpenJDK11U-jdk_x64_windows_hotspot_11.0.10_9.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (f12011de94a72e1f14c9e68ce63bdd537aab1bf51eb336eba6d6061bc307baeb) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f12011de94a72e1f14c9e68ce63bdd537aab1bf51eb336eba6d6061bc307baeb') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Feb 2021 18:00:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:62c48323ed8ac695b8cbe0ecedcc28ba185a234673ad9241df2b151dd00f9181`  
		Size: 1.7 GB (1725027107 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c03f1c41641d4a4cf6906dee9a590ee67135d926dddab80cfef993cae745a38a`  
		Last Modified: Wed, 10 Feb 2021 13:41:36 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8f84fbdf7025afe5c733dbdd9c6038db740d3ed5ee80ff83f12c045c7bb6fd`  
		Last Modified: Wed, 10 Feb 2021 18:54:00 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a32949f6e592301f6dcedb6f9f2bda9b5ef621fe13c7ca164c0c8408371ce7`  
		Last Modified: Wed, 10 Feb 2021 19:01:15 GMT  
		Size: 373.8 MB (373837656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c23e780053b38937857bd76fcd428bdc30f5f828a3036bada8e661e54e48740`  
		Last Modified: Wed, 10 Feb 2021 18:54:00 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
