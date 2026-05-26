## `openjdk:27-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:855770697504894479dcf4d7be6c60d709ce3a8cc578deece3330a98a6cabfaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:5b09bae3df6c7ef2ec5419e26fdaabeb707b177e57d2ef6332cf416c1a087116
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2348528572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf92ca682d8d4821c84ab5652c69e87648dadfde6beee6d13703acda1b13d99`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 26 May 2026 19:18:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 26 May 2026 19:19:37 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 26 May 2026 19:19:39 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 26 May 2026 19:19:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 26 May 2026 19:19:48 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 19:19:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/23/GPL/openjdk-27-ea+23_windows-x64_bin.zip
# Tue, 26 May 2026 19:19:50 GMT
ENV JAVA_SHA256=7a3570aa872e47b54f71fd9c142dc466b4b796ffc20ebd57cd26987efab6546f
# Tue, 26 May 2026 19:21:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 26 May 2026 19:21:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f74e31a73ad89127e60143561d9ad3841162a75b2db137fded34c76e7ce6180`  
		Last Modified: Tue, 26 May 2026 19:21:52 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c978d99f9d2ebbd2bcebb897c7a0836352eeb83a21a39101a03ce296ea6868`  
		Last Modified: Tue, 26 May 2026 19:21:53 GMT  
		Size: 514.0 KB (514011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e05ee2bf302da902b7dc3a8557b0c24d9cfc86a2337bb0f9ab7db6b578b97e`  
		Last Modified: Tue, 26 May 2026 19:21:52 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:def4c72472d0d1bf20cfca18565f32a020f15bd04adda548d44feb50dfc6f8b1`  
		Last Modified: Tue, 26 May 2026 19:21:52 GMT  
		Size: 314.2 KB (314221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef4f56301d3599e9fedfebc462669f428531ef54991adc24df444a8abf0c782`  
		Last Modified: Tue, 26 May 2026 19:21:50 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbd6e494f9dbb19dddf83893322b6b7000485e175c2edfe42dfd2f81e1d19b69`  
		Last Modified: Tue, 26 May 2026 19:21:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4b6212ee50cedd4a472cc1b3ac00ce7f25a4a1b1c1cbbbaa1d60303f28caf5`  
		Last Modified: Tue, 26 May 2026 19:21:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f31200730fbf78f26528841a93e8256d226a8d3f6d6d016549a956e1a854dd`  
		Last Modified: Tue, 26 May 2026 19:22:05 GMT  
		Size: 225.3 MB (225271918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9878a0fd2108acf4588dd354a30af5a7106b4f4e85dbc7ac60fb92024d8fce1f`  
		Last Modified: Tue, 26 May 2026 19:21:50 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
