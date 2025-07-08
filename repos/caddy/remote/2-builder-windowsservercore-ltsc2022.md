## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:8560a9c13225df7ffa874670caa1c3dafc5217ccc88b7d204c2cdf0a1f74f582
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull caddy@sha256:820f60e550760903a4703faac7a1cd9dad226ee9024824d77ff7397d34cebf9c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2411459097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59612f047de02209c8dc4abbbbd09fac810f59047f265e592bbaa3dd12071c03`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 08 Jul 2025 18:04:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Jul 2025 18:04:11 GMT
ENV GIT_VERSION=2.48.1
# Tue, 08 Jul 2025 18:04:12 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 08 Jul 2025 18:04:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 08 Jul 2025 18:04:14 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 08 Jul 2025 18:05:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 08 Jul 2025 18:05:31 GMT
ENV GOPATH=C:\go
# Tue, 08 Jul 2025 18:05:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 08 Jul 2025 18:05:42 GMT
ENV GOLANG_VERSION=1.23.11
# Tue, 08 Jul 2025 18:09:38 GMT
RUN $url = 'https://dl.google.com/go/go1.23.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1dbcf0b4183066550964b22890fe119b0b867b51f12c1eea4445c71494d98cbb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 08 Jul 2025 18:09:40 GMT
WORKDIR C:\go
# Tue, 08 Jul 2025 19:09:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 08 Jul 2025 19:09:26 GMT
ENV XCADDY_VERSION=v0.4.4
# Tue, 08 Jul 2025 19:09:28 GMT
ENV CADDY_VERSION=v2.10.0
# Tue, 08 Jul 2025 19:09:29 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 08 Jul 2025 19:09:51 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 08 Jul 2025 19:09:53 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541f19e23dae8d1ffe1ee23fca881849b841d34ae6a845614574a886f0b0218b`  
		Last Modified: Tue, 08 Jul 2025 19:07:53 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f7d18bd8e8e993aade1d728b301ca3d4f556cdaa66ff2b7adb1f05f689aead`  
		Last Modified: Tue, 08 Jul 2025 19:07:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aee5d610cf1146db0cab5f99d8c618193107a9bdf1dcbb17b2118202e807d8`  
		Last Modified: Tue, 08 Jul 2025 19:07:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4279c2b8713f98ab8fded7b4e4dd1ee34c1d3a2f55614ae52e57903543e8ad29`  
		Last Modified: Tue, 08 Jul 2025 19:07:54 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:056d34801f6addcd2e28fed489def285d8dc2a2b3acca21cc8c243a7cdb18d34`  
		Last Modified: Tue, 08 Jul 2025 19:07:54 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a00acded64c5b383b4dd98d879a564dd066ce5d712144eccc9e40d2785c81e`  
		Last Modified: Tue, 08 Jul 2025 19:08:01 GMT  
		Size: 51.2 MB (51214668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c601192a8ac4a02dcf8e371856d894ec01da7a3c7e8a86fe4f4f4e981d8cbb7`  
		Last Modified: Tue, 08 Jul 2025 19:07:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43827fa7fde0b027bb884b8a914acaae475522b42087a2cd73425bcbe84b96e6`  
		Last Modified: Tue, 08 Jul 2025 19:07:55 GMT  
		Size: 320.9 KB (320889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46cfd2ee5de9290f836943e0453194f861e49b55c7f5cb0d9d20517f4975e24c`  
		Last Modified: Tue, 08 Jul 2025 19:07:56 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28599aeb6358928201f6a96fb31238a265ebbdc59c9d9467bf6c97b655cd813f`  
		Last Modified: Tue, 08 Jul 2025 19:08:00 GMT  
		Size: 77.4 MB (77360750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e340d4b7a34ba05724e64e5e98dd0f5b8b03e25cbb02ee085f3abb0157c307f`  
		Last Modified: Tue, 08 Jul 2025 19:07:57 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d51a2aa210be002dc436ecae69bf0c7d5b416baa64331f2ac644572e61d632f9`  
		Last Modified: Tue, 08 Jul 2025 21:53:04 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0392f8ef037aeeaf4ae495d7c86256803179ed0771a682e5f1e07fc3015494b`  
		Last Modified: Tue, 08 Jul 2025 21:53:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2747a7cef5be9cdc71762622eb03ab0837f434b7c50e1709700114ba80d9be54`  
		Last Modified: Tue, 08 Jul 2025 21:53:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70d61a2eabc62edfc21e5ea64982f5a58a30d9b4a2edb890328c7b6b0ef2d87f`  
		Last Modified: Tue, 08 Jul 2025 21:53:08 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c20267e7eef8cbd0a22f8c9ed82d138a2de45795cb8a47e40d584686b920a1`  
		Last Modified: Tue, 08 Jul 2025 21:53:09 GMT  
		Size: 2.3 MB (2294326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68097b706593b367fa873d52172130e9147df921c37e834a49a11685763792d`  
		Last Modified: Tue, 08 Jul 2025 21:53:10 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
