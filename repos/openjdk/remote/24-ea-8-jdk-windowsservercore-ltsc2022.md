## `openjdk:24-ea-8-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:82a3f70acd9c9db6f9e93daf259dd6fff4a96e3ea2ee341565ebea00f1c0f23f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `openjdk:24-ea-8-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

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
