## `openjdk:25-ea-10-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:16e0ffb6b584e904414958393f3188e4c3586ce8ebe26e7165ab3b3d7b0e632e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `openjdk:25-ea-10-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:c30a31eb51414063a3fb71ff138ffa8512ecb9c22bb515e36779d648f262b20c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709000556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65afc8e5af227114cab13a4e5e4c691344fb47056373dc54a6cbcfd3c40a2c51`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 14 Feb 2025 23:32:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Feb 2025 23:33:00 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:33:01 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 14 Feb 2025 23:33:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:33:07 GMT
ENV JAVA_VERSION=25-ea+10
# Fri, 14 Feb 2025 23:33:08 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/10/GPL/openjdk-25-ea+10_windows-x64_bin.zip
# Fri, 14 Feb 2025 23:33:08 GMT
ENV JAVA_SHA256=9e8ebedd95dce7d5755f885b28067679019d529df9ff91b64e03edd7f2285e6e
# Fri, 14 Feb 2025 23:33:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 14 Feb 2025 23:33:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:630380736f07612a35719b61be2f0d4410c719defdfdf66326453933569f1456`  
		Last Modified: Sat, 15 Feb 2025 00:31:34 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b127f29d47d1334b45d3294161a389e791436052cbb1d5484e70980d6a23069`  
		Last Modified: Sat, 15 Feb 2025 00:31:35 GMT  
		Size: 384.9 KB (384875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6899a068a803177d37a7ed0dce5b252eca438ff80a6939a1779350c367a6d400`  
		Last Modified: Sat, 15 Feb 2025 00:31:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e8dd64f9c6078a3f54ab7cc9fd42c63fd8c36f9f4fa8f66e03846cd836bf28e`  
		Last Modified: Sat, 15 Feb 2025 00:31:36 GMT  
		Size: 373.7 KB (373671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82156f108d2eba6f3fc73bab750e13fdb781d4bbb99ff5b5e90a4fe7b0812ba`  
		Last Modified: Sat, 15 Feb 2025 00:31:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f6a1617d806f743adb4b0632a444418953c3b3a69c81aa55404e2902a3ba6a`  
		Last Modified: Sat, 15 Feb 2025 00:31:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be161ae7be15305731e6c5422ea7cfa28624c73a110830ed8a1bdfa1aafcf279`  
		Last Modified: Sat, 15 Feb 2025 00:31:38 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f3e00a0056f2cd5de9947f0dc389bedd030d0567397ba870566fec5cf4892b`  
		Last Modified: Sat, 15 Feb 2025 00:31:53 GMT  
		Size: 208.0 MB (207956604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a41399944e676da820aa319e71f292d2980c3c40c6674c50852734dd5fd9f40`  
		Last Modified: Sat, 15 Feb 2025 00:31:43 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
