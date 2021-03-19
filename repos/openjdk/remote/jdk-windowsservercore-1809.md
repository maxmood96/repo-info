## `openjdk:jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:f520c6e829e93123f030f7363a0b99c92a4e9c30a317e4c3103e3711c4b7e238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:jdk-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:64272b948aa8eee14c3796f20b1b29f882d0ff4ec5607cea8f035548f7685866
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2656120789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62debe7ef227780986f4e80ec062d7e68d392462f9f3c762bc0868724e047228`
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
# Wed, 10 Mar 2021 17:52:01 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 10 Mar 2021 17:52:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:52:27 GMT
ENV JAVA_VERSION=16
# Wed, 10 Mar 2021 17:52:28 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk16/7863447f0ab643c585b9bdebf67c69db/36/GPL/openjdk-16_windows-x64_bin.zip
# Wed, 10 Mar 2021 17:52:29 GMT
ENV JAVA_SHA256=a78bdeaad186297601edac6772d931224d7af6f682a43372e693c37020bd37d6
# Wed, 10 Mar 2021 17:53:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:53:41 GMT
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
	-	`sha256:99e972149e044aefd41b4e7257e94c617abb3999f22dc176273cac61a9c6a6d6`  
		Last Modified: Wed, 10 Mar 2021 18:35:06 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139b3cc0b70fd2cd536475109b74988b1899e087a304747891b1c8223d7872ba`  
		Last Modified: Wed, 10 Mar 2021 18:35:06 GMT  
		Size: 333.8 KB (333798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d2aa09c616c5ed8b1cdcd5198f30e7c17e72fba571f082a6123ea629b28e12`  
		Last Modified: Wed, 10 Mar 2021 18:35:02 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f4f6d2fa89d7f78141033fd8c301f03393b61266f3f911bada128ae9fff888`  
		Last Modified: Wed, 10 Mar 2021 18:35:03 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70205b27ab4cd8cddfd68de55b0258f8fcfe765c181e3ca95761338492afbe22`  
		Last Modified: Wed, 10 Mar 2021 18:35:03 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eee00ec39d40cbd81adbfb0a9c9c155fea7c469b7098de03f49a7aff9c6ed27`  
		Last Modified: Wed, 10 Mar 2021 18:35:26 GMT  
		Size: 184.8 MB (184786248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c570a15ba5115d05df4eedac77f448652e4e6f532e7c1ad82135cabb95110d`  
		Last Modified: Wed, 10 Mar 2021 18:35:02 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
