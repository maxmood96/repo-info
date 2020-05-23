## `openjdk:15-ea-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:f556a0a65f3eca1f84b555f0a17ca28665b4a39e46b894d6bbde2f757c3a5def
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1217; amd64

### `openjdk:15-ea-jdk-windowsservercore-1809` - windows version 10.0.17763.1217; amd64

```console
$ docker pull openjdk@sha256:8811f85dbf4eab286f98cf9aaa7162c7fc121f16132bddec6ae83d794eb28690
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1910616193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089852659bbb1e5e87e70fe0e92328592b0bd9b7826a3fdc9c16d702b329981b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-amd64
# Wed, 13 May 2020 12:41:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 15:22:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 13 May 2020 15:22:52 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 13 May 2020 15:23:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Sat, 23 May 2020 01:15:24 GMT
ENV JAVA_VERSION=15-ea+24
# Sat, 23 May 2020 01:15:25 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/24/GPL/openjdk-15-ea+24_windows-x64_bin.zip
# Sat, 23 May 2020 01:15:26 GMT
ENV JAVA_SHA256=058abe6c027572c237434b8a82d12b07cff7b4a304b7d784b1da73a48393e135
# Sat, 23 May 2020 01:17:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 23 May 2020 01:17:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:77613e754ba9d62c0acd4ef271c4ee7d3af091b8c8b310afa404560a9d281f82`  
		Last Modified: Wed, 13 May 2020 13:00:20 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc1950cbc28db7632bd0afe94e7afdd5ca08b3a3ca57687e6a837312b287f7a`  
		Last Modified: Wed, 13 May 2020 16:04:15 GMT  
		Size: 347.0 KB (346988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccd9bd22f75be58d6e2a85f96e44ed57e761dd5917328d2ab7a827a81241f7e`  
		Last Modified: Wed, 13 May 2020 16:04:15 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:928fd42a12a95b96ecfd3687faac5e7c17ace93c556f6920de761fb801902ada`  
		Last Modified: Wed, 13 May 2020 16:04:15 GMT  
		Size: 300.4 KB (300354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8675da8bad90838dbf1590728f262479c0ed7e94e5ecc19e625e7ca394964ca2`  
		Last Modified: Sat, 23 May 2020 01:25:30 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c27c441b96e16ae6c0ee76ce550c27432f50e2493435f97fe88fd5b154708ea`  
		Last Modified: Sat, 23 May 2020 01:25:30 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2888406cec9eb7d8f64f0be960c854b3d2aa5ef88f0e5751623131d7048cdca9`  
		Last Modified: Sat, 23 May 2020 01:25:29 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0efb2fc710393c323fad889320eebd0a2cea59fdbe4187563998794cdda9cd3`  
		Last Modified: Sat, 23 May 2020 01:25:52 GMT  
		Size: 191.6 MB (191629111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53dbde430dff6853830d6333223e2247da6713d8f009f09fd0b2725b435c80ef`  
		Last Modified: Sat, 23 May 2020 01:25:29 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
