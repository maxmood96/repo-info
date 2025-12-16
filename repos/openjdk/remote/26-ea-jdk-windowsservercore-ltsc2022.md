## `openjdk:26-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:0ecb01594fd6d601f6ecc289ef5dcb89ee876d8db368eb2180fe7e85d4998df4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `openjdk:26-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull openjdk@sha256:e1646488a9b1b10d5ff28a2f5e166c5ce53caa04fdb864c9ae7a34c959c79893
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2004956527 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb65ec2b9eff1a3203ea84526164e3d2202ca4e168572f16363ebb0ba5722ade`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 16 Dec 2025 00:16:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Dec 2025 00:17:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:17:19 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 16 Dec 2025 00:17:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:17:29 GMT
ENV JAVA_VERSION=26-ea+28
# Tue, 16 Dec 2025 00:17:31 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/28/GPL/openjdk-26-ea+28_windows-x64_bin.zip
# Tue, 16 Dec 2025 00:17:32 GMT
ENV JAVA_SHA256=1043a56a8e09613f76543d6e9290ff5c53e9cc2bcf0053550a36ad993843bf2c
# Tue, 16 Dec 2025 00:19:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 16 Dec 2025 00:19:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0164f5f587ba9e1d772302470d6e2a40b4db6de9f934fa05a050561fea3c6b`  
		Last Modified: Tue, 16 Dec 2025 00:32:11 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:633f413298b2e15783de0dc340c9b8e1057b64d330bca33fab54f4a4f01bd1d3`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 502.5 KB (502461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b8d8aaf15387684f2422021367394634513c8fbbcfd6572115f3312ea7cbcf`  
		Last Modified: Tue, 16 Dec 2025 00:32:11 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6721e2a2e399f5f0bf873896049e93dfac1dc0022a6acee0a772f927b74bc846`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 346.9 KB (346915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca57404cf8572be7ed887b827c077822a5ebce9ce65662a2b496f3880628f4a3`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8edbbdfa69d7626c275be4163e44bbd10b2efe5e72d102aabdacb97d7a70af44`  
		Last Modified: Tue, 16 Dec 2025 00:32:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d696c6e66f21ce3e4d558d98e1c9241243ae96ff18a2731a0ca9be8096d41b`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73aedb3f184b67dd44a6688d0fb685bd8ded0d73c956fd0a4b0061510219954`  
		Last Modified: Tue, 16 Dec 2025 00:32:19 GMT  
		Size: 224.2 MB (224220002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fe3af75bdb2e869e4d973178a330d7123679be81da876c263fbb8991fbb794`  
		Last Modified: Tue, 16 Dec 2025 00:32:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
