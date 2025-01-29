## `openjdk:24-ea-33-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:29ac4203ef685ccce7a8ffb9a76dde68dede28f1da00d117a0193bd459576f95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-33-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:7784925c0750f526f04e289795934de9d268924cf7a856e71acbcbde42d68d34
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331791117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:366650b25b20c7cf6aed69c14f986613410668d47adebe2f4a8bc1637e9dfe8d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 29 Jan 2025 00:26:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 Jan 2025 00:27:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:27:16 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 29 Jan 2025 00:27:27 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:27:27 GMT
ENV JAVA_VERSION=24-ea+33
# Wed, 29 Jan 2025 00:27:28 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/33/GPL/openjdk-24-ea+33_windows-x64_bin.zip
# Wed, 29 Jan 2025 00:27:28 GMT
ENV JAVA_SHA256=2c9091018c7bf3181421a86a3aabfe9ea9c375ed3720c8525be78fb54aa5516d
# Wed, 29 Jan 2025 00:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 29 Jan 2025 00:28:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b45ad8977ecedbed3551fe50628634c7b642dff09edaef7c578f46ccd713678`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a18d24266ecf7e243cf8f1581c183c199b36df2ec7608d9771cfd3c243f9d78`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 355.8 KB (355794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13be41d7f083912bf80ed0bd2351108d217b1354ae511aafe43b63cc36567dda`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc20b4c63913d1beddf987e9684863af1a07caf815239f136b07e7fa8daa9e33`  
		Last Modified: Wed, 29 Jan 2025 00:28:09 GMT  
		Size: 347.2 KB (347248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df63609e1edbeea706f421e15e7e4f8108282ff53c53dbe89875328ab43a28ba`  
		Last Modified: Wed, 29 Jan 2025 00:28:08 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a850c800b16adf102f4c1bc38c9613331d42eb6f1884679229af705630d5e6a`  
		Last Modified: Wed, 29 Jan 2025 00:28:08 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17818212bc6429994777faf3321863bd25160ab2689225b88cf332796bb3f8e3`  
		Last Modified: Wed, 29 Jan 2025 00:28:08 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f9eee6fa0968ff59355d7cfcb991e71936b5b5aac99d24f468b0255e79297c`  
		Last Modified: Wed, 29 Jan 2025 00:28:18 GMT  
		Size: 208.9 MB (208867943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ff5ec3277a510f8072f0c6c8b526e8c5bd2998b8e905d1208da741cef4cd9f`  
		Last Modified: Wed, 29 Jan 2025 00:28:08 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
