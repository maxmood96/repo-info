## `openjdk:23-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:deb0d9ca63f5bb64900918c88a669a06bfe45bbe443509f59405f35ff719cbc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `openjdk:23-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull openjdk@sha256:0d06ce55d03223da6ab27f2b5c224dac8566c1c0269381bcdd1c17a6986df9db
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2319620310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c883dbab00fd5e32b71d78f2057facf28ee9b4ba3415aa2c0105ee74f17f09bb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Mon, 03 Jun 2024 19:00:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 03 Jun 2024 19:01:51 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 03 Jun 2024 19:01:52 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 03 Jun 2024 19:02:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 03 Jun 2024 19:02:01 GMT
ENV JAVA_VERSION=23-ea+25
# Mon, 03 Jun 2024 19:02:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/25/GPL/openjdk-23-ea+25_windows-x64_bin.zip
# Mon, 03 Jun 2024 19:02:02 GMT
ENV JAVA_SHA256=31f40e7502496063307f37470402eeb3c2e5a3ee3babece396655f9e0056c8b1
# Mon, 03 Jun 2024 19:02:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 03 Jun 2024 19:02:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540a0354b3436f736d77efebc2e96cfd569f232bf0f16440b16e7b4f8bdab5ec`  
		Last Modified: Mon, 03 Jun 2024 19:02:40 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc7b64aa26cbdea5cb89ab2f8af4799dc4e51b7b799207e9ae74838923bbde5`  
		Last Modified: Mon, 03 Jun 2024 19:02:41 GMT  
		Size: 351.1 KB (351056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510645546c3e41b327e88d54f7f6f5d8706fa572ac73bb06a804b1112374aae5`  
		Last Modified: Mon, 03 Jun 2024 19:02:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d655cf89f8f4243af0f3fc20ca797de27bd42f0a88f808a1cbf728e3d91957`  
		Last Modified: Mon, 03 Jun 2024 19:02:40 GMT  
		Size: 300.7 KB (300674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcb35852b6a96888a55fc17e3b28335133e4d748ba8a6842762f378a0786ea68`  
		Last Modified: Mon, 03 Jun 2024 19:02:38 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de4d870d49f9f867a16a9592c6e4c03a2e9ef7f1325fa7d0789a73baf1d3ede3`  
		Last Modified: Mon, 03 Jun 2024 19:02:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1451c1d769179e0460029bc4ddd122b12a63a99ace9d6d6664e981c5bbbc63`  
		Last Modified: Mon, 03 Jun 2024 19:02:38 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0554bf5730b63e015528a1e9ccdeeb5bef9bee34fec2435684a0ad4875704219`  
		Last Modified: Mon, 03 Jun 2024 19:02:50 GMT  
		Size: 206.3 MB (206289454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946112fa51cae28a1f8e886ee6dcaf07acea6be2bd7f1908b17c50f885cc48ba`  
		Last Modified: Mon, 03 Jun 2024 19:02:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
