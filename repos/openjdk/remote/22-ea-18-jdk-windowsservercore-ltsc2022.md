## `openjdk:22-ea-18-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:731c16496b31496c95163c185721053d9f9fafd3de103ab493b6cd880d3bb8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `openjdk:22-ea-18-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull openjdk@sha256:21ead4c37600f78c748dbe4da4a4c42d55fc4dd2cc7a0ccc672b36ef36d51a20
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2037437444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aca550af4ef2ea638c7f86174dfd2f1b31678e8fdaef59fde38821ee751ec6dc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 01 Sep 2023 00:43:48 GMT
RUN Install update 10.0.20348.1970
# Wed, 13 Sep 2023 01:35:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Sep 2023 05:14:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 13 Sep 2023 05:14:16 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 13 Sep 2023 05:14:36 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 06 Oct 2023 19:22:40 GMT
ENV JAVA_VERSION=22-ea+18
# Fri, 06 Oct 2023 19:22:41 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/18/GPL/openjdk-22-ea+18_windows-x64_bin.zip
# Fri, 06 Oct 2023 19:22:41 GMT
ENV JAVA_SHA256=9514da1d60086946d1324cfabda5280213d7243eec44e2268bbbf02248d910ff
# Fri, 06 Oct 2023 19:23:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 06 Oct 2023 19:23:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feca8e06011ab171ad74cda49c7c305e791965aef283d5b7c2b987dd5388e6c7`  
		Last Modified: Tue, 12 Sep 2023 18:24:42 GMT  
		Size: 448.7 MB (448675362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f40969dbf1e035a6c49e7c40b216960e3ee98ec3b76f76f9fe4498d0110bee`  
		Last Modified: Wed, 13 Sep 2023 02:15:22 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b411249ef1c74d6763984f0b9b085ac311c6e49aba35a7dbbc1d42264a11ba`  
		Last Modified: Wed, 13 Sep 2023 05:25:31 GMT  
		Size: 462.9 KB (462878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d5d90c5ae40ed0401706ba6915059213a0cc520cc862f8fdbff4e582cbc835`  
		Last Modified: Wed, 13 Sep 2023 05:25:31 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84e7bb658094bff788d92f8ca930570e83805ce31d072d4c675acbef78b62b`  
		Last Modified: Wed, 13 Sep 2023 05:25:31 GMT  
		Size: 274.9 KB (274889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5183453d52f48d4566cca8c148af7c366e9f49319e6ada23452c88d89c393cf8`  
		Last Modified: Fri, 06 Oct 2023 19:26:56 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d35f0b838e4b4ebce3404ba5519e64397f22c6a0ef5f5502c6fd119df58882`  
		Last Modified: Fri, 06 Oct 2023 19:26:55 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb1826af811d247dd1a729717f715141f1fea0068cb427655fefdcb42995acd3`  
		Last Modified: Fri, 06 Oct 2023 19:26:56 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7790dad9e18b808741f949055a5374d537d0b0ba722b0cd439557aa595929d10`  
		Last Modified: Fri, 06 Oct 2023 19:27:13 GMT  
		Size: 199.4 MB (199417252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:572bb338c95cd876a95d56b0d43ee49245d63e4d650c0f8a910abda858bd3797`  
		Last Modified: Fri, 06 Oct 2023 19:26:55 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
