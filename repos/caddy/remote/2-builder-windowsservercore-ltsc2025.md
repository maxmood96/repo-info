## `caddy:2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:f3a7bda7baf4656ca89644d17f9115977f9bc387ac883429bc4e65ebcb75ff46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `caddy:2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull caddy@sha256:37ed736284e56457e89c30926c1257594d397979614fa28e29e51899c27ed628
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3615337218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71482ccb5d5af02699b97417cfd4f52c3c33539b15ef2c581fb7e935f781901a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Wed, 03 Sep 2025 18:54:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Sep 2025 18:54:11 GMT
ENV GIT_VERSION=2.48.1
# Wed, 03 Sep 2025 18:54:12 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 03 Sep 2025 18:54:13 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 03 Sep 2025 18:54:14 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 03 Sep 2025 18:54:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:54:32 GMT
ENV GOPATH=C:\go
# Wed, 03 Sep 2025 18:54:40 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 03 Sep 2025 18:54:41 GMT
ENV GOLANG_VERSION=1.25.1
# Wed, 03 Sep 2025 18:56:23 GMT
RUN $url = 'https://dl.google.com/go/go1.25.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '4a974de310e7ee1d523d2fcedb114ba5fa75408c98eb3652023e55ccf3fa7cab'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 03 Sep 2025 18:56:24 GMT
WORKDIR C:\go
# Wed, 03 Sep 2025 19:11:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Sep 2025 19:11:13 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Sep 2025 19:11:15 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 03 Sep 2025 19:11:16 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Sep 2025 19:11:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Sep 2025 19:11:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f495bbd35ca8371e7ec2ae6c370e5682cb4115fab536c9282a01229768afc4`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43216771afdda44565d262c41cb4e449d6be29edd33e3e8bb55360a9da328d53`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a19e361e0b9d583cb99cba5f0bc5e433894e70eb6bcfd03408daa7e0513885`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc3cdf339cc1b15f23e17648fb50e6dfa0a82edee34b12a0edc43f3304b8f8c`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a59f12ead65b3b97d30afe4e69cd209e7eb29dadd77a965d9616f7e60f3ccab`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1920035ea1acffe071d8a1a6e540cbc05a2227b03f219f5f60cfeea15d4f5a2`  
		Last Modified: Wed, 03 Sep 2025 18:59:55 GMT  
		Size: 51.3 MB (51255221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6209f159116204b114dc0a4ee1f3c7ab824b77eeb134fa89a6c4db43f33457ab`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520317e2ec06ea76cc88364e82fab6db4e97c7a1f8841409d5bad1ed377db1ab`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 376.9 KB (376942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88b200dd9d7936388cee63e986533a5e6f4c5cd3e17fd0cd0c8ce10689499288`  
		Last Modified: Wed, 03 Sep 2025 18:59:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e66a3739df18124532e005e6e2f676fee662b557add1fb9f756e2fa1aa3a235`  
		Last Modified: Wed, 03 Sep 2025 19:00:01 GMT  
		Size: 62.5 MB (62497761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d4085daa7946c18453d6431bca13352e3a418408ce342846fab2a53a4750e3`  
		Last Modified: Wed, 03 Sep 2025 18:59:55 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4bf37adc617b100596b6a009b9fdfb4704df92567918df0860d843e837614c`  
		Last Modified: Wed, 03 Sep 2025 19:12:00 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6739503020df128d5a7c8c2b1703f54d6bcf8f07e266c9e36f71218257de2aad`  
		Last Modified: Wed, 03 Sep 2025 19:12:01 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34327dfc9e027bd4fb48ecc98431f030b8805d7cabcd6e9d06c07da75c830573`  
		Last Modified: Wed, 03 Sep 2025 19:12:01 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee194ebeba1a7109f4c0e3411aa368bd73a494a319a134bd9526f64623ac5808`  
		Last Modified: Wed, 03 Sep 2025 19:12:01 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538c8dc90ad4deeb81b118eaf911a780b0a098cbf0020a22c20254ffe09a5880`  
		Last Modified: Wed, 03 Sep 2025 19:12:02 GMT  
		Size: 2.4 MB (2359656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a274434bed633e280c8a09f9223295eee584629c55942b864767c8069a4e7b8`  
		Last Modified: Wed, 03 Sep 2025 19:12:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
