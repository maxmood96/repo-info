## `openjdk:25-ea-4-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:ed4feb90a485ac4bc14cfeaacec24a127f55cc617ade83e5d97af07b19fc0ae6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `openjdk:25-ea-4-jdk-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull openjdk@sha256:37756ff96bbdc664bbeb90f2875249af725c5ffb2f5c102a502b92b23b51ff03
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2224012853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3baa9b0e3404726684b22b74bb8306c20e91fb2d16398f53d3c0364a517142ec`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Mon, 06 Jan 2025 20:27:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Jan 2025 20:28:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:28:58 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 06 Jan 2025 20:29:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:29:06 GMT
ENV JAVA_VERSION=25-ea+4
# Mon, 06 Jan 2025 20:29:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/4/GPL/openjdk-25-ea+4_windows-x64_bin.zip
# Mon, 06 Jan 2025 20:29:08 GMT
ENV JAVA_SHA256=a269f89b8b7317bbeea0e0df24e66a537aa1762f6b13db3da0fff25ce714ab98
# Mon, 06 Jan 2025 20:29:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Jan 2025 20:29:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e9c28c64c5934715727e50f34212b6ce7722ecdadbc6853c2f0703cd76067c`  
		Last Modified: Mon, 06 Jan 2025 20:29:59 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1805afc196d9b719a68a1d2f78e8728c2a1e3a280bfeb6dcafa622585187eef0`  
		Last Modified: Mon, 06 Jan 2025 20:29:59 GMT  
		Size: 486.2 KB (486242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea14f5040ebfab52b413a5cfc758dc7c1a038b6a94c919a3eb573a231ab9e3b`  
		Last Modified: Mon, 06 Jan 2025 20:29:59 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4662df3f4b234415b2caece2cc2725d6a703371c33c1b531252fd053c46b67`  
		Last Modified: Mon, 06 Jan 2025 20:29:59 GMT  
		Size: 338.5 KB (338487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6509f0be496765d86091492a39222eba375b2f89c6cf946587d0995b9771c6e8`  
		Last Modified: Mon, 06 Jan 2025 20:29:58 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95597edd1e8852b6182af65e7052f860e24b6539b0a604dfb728c20d1b53af1`  
		Last Modified: Mon, 06 Jan 2025 20:29:58 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53a0967a33a27e0770d39c47d2fb24e6ce5524c8c705be4ed2826111e7f6227`  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2579ec8940e6a9de984264e9e0aadc357371b8a6045be3c7a830326a58b5595`  
		Last Modified: Mon, 06 Jan 2025 20:30:11 GMT  
		Size: 209.0 MB (209010082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d75680458716856ccb9da8c04fcadef1220048d6dede019dd0b54549f2e3804`  
		Last Modified: Mon, 06 Jan 2025 20:29:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
