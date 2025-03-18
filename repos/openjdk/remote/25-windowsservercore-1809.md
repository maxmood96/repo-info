## `openjdk:25-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:26efefc31a9d8b633537641d504a4f0216a5cff07a10838035df27cd81491a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:2db8809ea2bd63d825d214e68cd138cf8f335db83e1ba2bb17e71c46b6639abe
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2360153366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3602d7d3a5a48efd4fb7c98f00e56813e7fa1ae00bd3e19b23162df067d60e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Mon, 17 Mar 2025 21:16:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 17 Mar 2025 21:16:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:16:58 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 17 Mar 2025 21:17:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:17:05 GMT
ENV JAVA_VERSION=25-ea+14
# Mon, 17 Mar 2025 21:17:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/14/GPL/openjdk-25-ea+14_windows-x64_bin.zip
# Mon, 17 Mar 2025 21:17:06 GMT
ENV JAVA_SHA256=4616b55a7c0d6b65d650a08986609158fbffcfed8fc5fa589e9f356898d735d0
# Mon, 17 Mar 2025 21:17:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 17 Mar 2025 21:17:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b63c86f7839a930dbd1846acfd3ad4b1a64a13f6b576c382b05fd1939375f15`  
		Last Modified: Mon, 17 Mar 2025 21:17:34 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a0c80b8e1d84918f51d0dcddc9763d92bd252cfd0fb95b1059b76a115141409`  
		Last Modified: Mon, 17 Mar 2025 21:17:34 GMT  
		Size: 340.6 KB (340643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f68dd6cd9e38825b3d1d90daa7b55cc2802e01d6c6e8a01f399916fadcbbbb38`  
		Last Modified: Mon, 17 Mar 2025 21:17:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71af051fd9a3191b2dafedb8742e7e48ccaa574afebc3962c72f765ec74b003b`  
		Last Modified: Mon, 17 Mar 2025 21:17:34 GMT  
		Size: 331.3 KB (331315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:245ac7785c6f9900bc46db349c250a68344bc18f8b36903b7461575422d9327b`  
		Last Modified: Mon, 17 Mar 2025 21:17:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0769b485ed16adb6e79150c889bd1633c5148fe06257866651a2d92c636a7f1`  
		Last Modified: Mon, 17 Mar 2025 21:17:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d9b21ec5a23a3abe941d46a4330382e7f7e0f171ad11222577efd9f6cbcc83`  
		Last Modified: Mon, 17 Mar 2025 21:17:32 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7983c95fae05d038284d0d189b03edb6c7ac0b0cf1e29c3ee5beb1782d4f8b2`  
		Last Modified: Mon, 17 Mar 2025 21:17:45 GMT  
		Size: 207.8 MB (207839003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a725c431b934368e5a5ee950494040a14f945ab97fed4d6e774812b2ff779e5`  
		Last Modified: Mon, 17 Mar 2025 21:17:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
