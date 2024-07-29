## `openjdk:24-windowsservercore`

```console
$ docker pull openjdk@sha256:2928acbdf6d9238d5361f67d3ec23aa45c01abe1efbaff04f8e9eda9db3f4975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `openjdk:24-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:47ac10c1c92881f1a734baa9c1a43d308f473821759f72db3e2f176399068b67
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2347131064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b36c03ec934cd4bbbe15293641ffdf0a4ebb6bc3445d706afc27a1566d71ba2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Mon, 29 Jul 2024 16:56:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Jul 2024 16:57:33 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:57:34 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 29 Jul 2024 16:57:41 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:57:41 GMT
ENV JAVA_VERSION=24-ea+8
# Mon, 29 Jul 2024 16:57:42 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_windows-x64_bin.zip
# Mon, 29 Jul 2024 16:57:43 GMT
ENV JAVA_SHA256=9b41f4fa8fda2053a051bc20bddfb268fafd41238d79bbe06fe4e295fdafa5de
# Mon, 29 Jul 2024 16:58:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:58:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95de3cbbf001e64065f33024bb9fc66f601b201a1bd13f8e955fb59e548cd08f`  
		Last Modified: Mon, 29 Jul 2024 16:58:27 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfb10e03948900098a30d8b7b3e19c890bddbbdef4787079175672bf40d47ace`  
		Last Modified: Mon, 29 Jul 2024 16:58:27 GMT  
		Size: 350.3 KB (350324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523949db16d8452518ae7866fd9cbef7b43e83775375d3505c5263abbad8b036`  
		Last Modified: Mon, 29 Jul 2024 16:58:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a57ac7d0467e556e36c8356b84448cac1a068d48b0271ec4d78b4574d9b8dad`  
		Last Modified: Mon, 29 Jul 2024 16:58:27 GMT  
		Size: 301.5 KB (301452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e1709f1edf9097ae9d5ace66214ae94a0b75e94b506ee67bef409fa59eb7c`  
		Last Modified: Mon, 29 Jul 2024 16:58:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7842f9460a31ff6257b5108993a4cbb21f63935b5426aad589fc44016ec20465`  
		Last Modified: Mon, 29 Jul 2024 16:58:26 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41ab2b6ff304579be2e31e4b094b51b8f03d2396b25068926078b993db48e5a`  
		Last Modified: Mon, 29 Jul 2024 16:58:26 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff82a309975eb5e6385ff3b523158292ede1fafdcbcc0eed517fa356eb16942`  
		Last Modified: Mon, 29 Jul 2024 16:58:36 GMT  
		Size: 206.9 MB (206871068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:869e296a5c02dff6f818ccff0d0b7ffabebc2721fe6a35520c7ae01ae184844d`  
		Last Modified: Mon, 29 Jul 2024 16:58:26 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:95baa02d981cdef0ef50d780dc9c0022f9b582014bde6fd88249183bf50be3a3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2446207553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bd87c7f337db9ca90e9ee277dd34d224989171265563be0b014235347d9286`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Mon, 29 Jul 2024 16:56:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 29 Jul 2024 16:57:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:57:50 GMT
ENV JAVA_HOME=C:\openjdk-24
# Mon, 29 Jul 2024 16:58:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:58:10 GMT
ENV JAVA_VERSION=24-ea+8
# Mon, 29 Jul 2024 16:58:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/8/GPL/openjdk-24-ea+8_windows-x64_bin.zip
# Mon, 29 Jul 2024 16:58:11 GMT
ENV JAVA_SHA256=9b41f4fa8fda2053a051bc20bddfb268fafd41238d79bbe06fe4e295fdafa5de
# Mon, 29 Jul 2024 16:58:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 29 Jul 2024 16:58:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53b783b0cf8e37b2c0f00564cca28d5eeb16f5631d32c46158602725e5aafd4`  
		Last Modified: Mon, 29 Jul 2024 16:59:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c64b0e61aae45e76d9def9ee6c845d9ed3d0fba666d102c4433a17a104fbed`  
		Last Modified: Mon, 29 Jul 2024 16:59:02 GMT  
		Size: 498.4 KB (498409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369b1b8250d40d63bc281c263adc432030d9bb2978aa4c9487b179cae6171635`  
		Last Modified: Mon, 29 Jul 2024 16:59:02 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c83efdc57a70c17b5bf63ac8781481059779db32f8001d6d3ef18b2eeea2d53`  
		Last Modified: Mon, 29 Jul 2024 16:59:02 GMT  
		Size: 343.0 KB (342991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5a267aca3004e64a2a5367d18f36b612dbae0d83c774d63d3e660d5df9c22c`  
		Last Modified: Mon, 29 Jul 2024 16:59:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6daaf2aa5e66fb7d58c5d0411522d77d9142fe5fd9f85a466f3a0857f163c701`  
		Last Modified: Mon, 29 Jul 2024 16:59:00 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a03386bf4ae3045571e3824f0f87625aeff932644f37d9212d96e0b96533fc`  
		Last Modified: Mon, 29 Jul 2024 16:59:00 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527612a864b1bd69941cf732d530674a883fa13f00a3722bcde983ef3071d059`  
		Last Modified: Mon, 29 Jul 2024 16:59:12 GMT  
		Size: 206.9 MB (206928962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a215bb5eaa00884df78cde1c704bbb2900ff015a214bb9cd297457a2bf3730d`  
		Last Modified: Mon, 29 Jul 2024 16:59:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
