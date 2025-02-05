## `openjdk:24-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:81001ebfba14a36be69a9980f4dfc274041f5d3493c8712ad3c170c6fc2f0656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:d623f8dbcf1bd1ffb70172a44c8489cd3561e09558e3dbc537fe7a2dfe2777a0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331789524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afd9d83614222ca5fa91c2d5a82a8e281893762529c5e8b22b1b5b82e28f3a0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 04 Feb 2025 23:31:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Feb 2025 23:32:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:32:57 GMT
ENV JAVA_HOME=C:\openjdk-24
# Tue, 04 Feb 2025 23:33:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:33:10 GMT
ENV JAVA_VERSION=24-ea+35
# Tue, 04 Feb 2025 23:33:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/35/GPL/openjdk-24-ea+35_windows-x64_bin.zip
# Tue, 04 Feb 2025 23:33:12 GMT
ENV JAVA_SHA256=1d56c9650251685d5d3007781088385fe316738b84a354ef2d3a42b83a38bd46
# Tue, 04 Feb 2025 23:33:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 04 Feb 2025 23:33:56 GMT
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
	-	`sha256:2d9eefe89536b84b640bc3328da635887d46a08366f45c3c9ed76c7dab41e6bd`  
		Last Modified: Tue, 04 Feb 2025 23:34:01 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238ccb5f45f9b6fe33def8b28972062451c43b5eeb5c1aabfba3b889f6d370cf`  
		Last Modified: Tue, 04 Feb 2025 23:34:00 GMT  
		Size: 341.7 KB (341688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4793b5cc4cc0e5e73b287b7abbe099c62364d2410843fe04663f5f1ae83a5e93`  
		Last Modified: Tue, 04 Feb 2025 23:34:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f864f2021d9f4aefe4404683dfd532a5d961bffbafd40811a4ce13786c8303d`  
		Last Modified: Tue, 04 Feb 2025 23:34:00 GMT  
		Size: 332.1 KB (332072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c5e5ef8c1fdc6b7d53a379033c860556ca88444ad4336ba7556f5c569e6706`  
		Last Modified: Tue, 04 Feb 2025 23:33:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e94a33006fbc0793982ece6ba767dc8f05627caa205dfd779402b704d44407`  
		Last Modified: Tue, 04 Feb 2025 23:33:59 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5abd32a8823fe8443dfc616eeb9cb17ff024878729bba6333da9bd0927551`  
		Last Modified: Tue, 04 Feb 2025 23:33:59 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81caaf5e64f03c1b93a1468f2303566f8e209ce483f88efc04eb1ae7802c3374`  
		Last Modified: Tue, 04 Feb 2025 23:34:10 GMT  
		Size: 208.9 MB (208895780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55483bc13561a9fd6f8d9b4da538e3e96d28f32641a0a3ae84d0c56480295723`  
		Last Modified: Tue, 04 Feb 2025 23:33:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
