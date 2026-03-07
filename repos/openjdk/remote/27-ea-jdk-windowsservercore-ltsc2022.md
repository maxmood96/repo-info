## `openjdk:27-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:6d3e7a7b5d93d42720e90dded962e84ff0d207ebbe106bfd7a815cb12b70c26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:659be96f4b08263e91fbdffe619c61b6cfb3fa2c7e20cbf823641e41da2375b6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088264222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6914f939873051b3b4185fc30ee9b4814381612c4b31020f80da867841b723a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Sat, 07 Mar 2026 00:43:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 07 Mar 2026 00:43:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 07 Mar 2026 00:43:43 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 07 Mar 2026 00:43:51 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 07 Mar 2026 00:43:52 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 00:43:52 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/12/GPL/openjdk-27-ea+12_windows-x64_bin.zip
# Sat, 07 Mar 2026 00:43:53 GMT
ENV JAVA_SHA256=bb5331abf59ac46c0dd11cefa00cc052f8d7cf6384d850b919591cb3346acbe4
# Sat, 07 Mar 2026 00:45:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 07 Mar 2026 00:45:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc6e8dba04deb4778bb53227d2f2b7d36d3ec9dbd6c229dae635f7a1ef347b4f`  
		Last Modified: Sat, 07 Mar 2026 00:45:25 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:816998ede68709017432c727cfadb1218e0b2f6fec64343c3bc4132edcf9db7a`  
		Last Modified: Sat, 07 Mar 2026 00:45:25 GMT  
		Size: 511.2 KB (511199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92907900c89948b025f256bbc02c99f5a70461413ef8209fbd86f5a02ed50dad`  
		Last Modified: Sat, 07 Mar 2026 00:45:24 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8204cc39f72950db2a0b24e0aa9f22c94fd32d0e2340acefdc34b3bd8063b6`  
		Last Modified: Sat, 07 Mar 2026 00:45:25 GMT  
		Size: 350.1 KB (350099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4f0899f472cfaa750c1590d8ff62ad552400c15585284b11f4ce4cec550189`  
		Last Modified: Sat, 07 Mar 2026 00:45:23 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4d2ce9d9fe41b7f5892c89a27f75609a55a464c89e8c607d43438adabb76308`  
		Last Modified: Sat, 07 Mar 2026 00:45:23 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d31e5ddfe67002e1307e64a9d2f9abd276d1983c7c5b31ca56f1699a2442bc74`  
		Last Modified: Sat, 07 Mar 2026 00:45:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47334ad792e6a1e14c9ad824e9821985935433f97d1db0e229a8525ba12e032b`  
		Last Modified: Sat, 07 Mar 2026 00:45:39 GMT  
		Size: 224.7 MB (224737832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65da38bd43be05c70506d0c895a02e43b074196bb198f2619da21a9e31520a3`  
		Last Modified: Sat, 07 Mar 2026 00:45:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
