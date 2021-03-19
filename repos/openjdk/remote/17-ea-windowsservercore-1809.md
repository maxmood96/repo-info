## `openjdk:17-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:1a161317e2c8d8d7c7cd818855da7ec580e2dd8f7e00f9b09a2291d914e1eb77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:17-ea-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:6bfe0dbbbe66b451efdba3b2b72f50374debdf2a1ffb9720f87bf649ff90ea57
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2656737897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98860d72e0448b28a083461dde2f42c5f55ab46888636635209a4c1397aa31e8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 17:43:17 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:43:18 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Mar 2021 17:43:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 19 Mar 2021 19:15:27 GMT
ENV JAVA_VERSION=17-ea+14
# Fri, 19 Mar 2021 19:15:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/14/GPL/openjdk-17-ea+14_windows-x64_bin.zip
# Fri, 19 Mar 2021 19:15:29 GMT
ENV JAVA_SHA256=bb67e52010e2fcab6f54a97cf4b9124b66ae27bb3f2edc17a77a0a681e6b166e
# Fri, 19 Mar 2021 19:16:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 19 Mar 2021 19:16:42 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef5a565fbc6dee6b0e5a6252ca763370a8d3521925db3d451dd6e7ec0efc1b07`  
		Last Modified: Wed, 10 Mar 2021 18:28:58 GMT  
		Size: 9.5 MB (9457788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce65a7afaa8a843f59f4e00b2cde68e50c25b4931a7ce73ff3b55438bd7742bf`  
		Last Modified: Wed, 10 Mar 2021 18:28:54 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2620c5b70d10c22e375ff81365a7e5c381fd1cb523ae714bcb824d42a5a46c51`  
		Last Modified: Wed, 10 Mar 2021 18:28:55 GMT  
		Size: 334.1 KB (334116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02be5c23bd235d6f3e9560c98e9c473206f30a8291eedb2c4243917759008d80`  
		Last Modified: Fri, 19 Mar 2021 19:26:47 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5776f96dfb772a36e48d590af566ebc49854542a7581323712c2fc9bb49874c`  
		Last Modified: Fri, 19 Mar 2021 19:26:47 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e803b79b97660a318906df4dece9970eea604be8eae59811a92eda1b3c698d8`  
		Last Modified: Fri, 19 Mar 2021 19:26:47 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d455578ca38563e31b214ac87b4b665c216a507bc9986b6f2b91dd54f12d88aa`  
		Last Modified: Fri, 19 Mar 2021 19:27:08 GMT  
		Size: 185.4 MB (185403020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5cb193f6e98740333137fd49752e8ea1ef9476f1dc4d499a1fd8fa154b69a7e`  
		Last Modified: Fri, 19 Mar 2021 19:26:47 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
