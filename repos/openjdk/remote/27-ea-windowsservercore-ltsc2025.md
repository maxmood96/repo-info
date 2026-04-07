## `openjdk:27-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:40ff6fa424d46a5e0b61f58118a8690f3733e37ae671371f385c34355b4e591a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:27-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:26e06e40e8a0cecdc4e509e0b829efae6c8496b0aa9eed3e9e7afe5f6446da0e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2307108797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8570d771ed3a0584de0ff1ce1ff9598208de75790b6c25f1a315118c58645038`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 06 Apr 2026 18:26:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Apr 2026 18:27:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:27:19 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 06 Apr 2026 18:27:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:27:27 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:27:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_windows-x64_bin.zip
# Mon, 06 Apr 2026 18:27:29 GMT
ENV JAVA_SHA256=e5c718947519c88a2ee3b23aea3ed1da5b81b674c4f03fe8b29395ab126d36ef
# Mon, 06 Apr 2026 18:28:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:28:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7157efab2f341875530685270a8e3ebd68d46fce725e5023b31f0ab24bff80`  
		Last Modified: Mon, 06 Apr 2026 18:28:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:609aaed14f2f94e01ab3704870a1faa711744e29a7b05512e7bd7e25f5989eaa`  
		Last Modified: Mon, 06 Apr 2026 18:28:35 GMT  
		Size: 388.1 KB (388057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9773285db393376a2da37442199f23b414c9b2789c64e40616b6d2009b2e7eb`  
		Last Modified: Mon, 06 Apr 2026 18:28:34 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a247f5112c541e9a7326e4a8ebd607f035883872d142c077bf185237f3a2f05`  
		Last Modified: Mon, 06 Apr 2026 18:28:35 GMT  
		Size: 369.8 KB (369774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8adf67f58f5f31c6d1ab31ad6488ceabaf57de5137a53c4978adc565127d28`  
		Last Modified: Mon, 06 Apr 2026 18:28:33 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057362a51559414a1bf3bbb6adafeab82ad9e9beed098fb2206cb097201fb009`  
		Last Modified: Mon, 06 Apr 2026 18:28:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41bb8e536e0a07f45ea489905239d15cc2e99cc27219c82aba97c233c2e54568`  
		Last Modified: Mon, 06 Apr 2026 18:28:33 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0395289ca06d1f4ef950720934332cba4b8360c360c6a96907379c1d3fb99bf6`  
		Last Modified: Mon, 06 Apr 2026 18:28:49 GMT  
		Size: 225.1 MB (225147060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56253a51a86d37d215981a3c700e73e0b606af875fa0cd11e100a2244a6239c2`  
		Last Modified: Mon, 06 Apr 2026 18:28:33 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
