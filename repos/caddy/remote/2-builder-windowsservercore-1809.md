## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:cffc4903a82f1dc8932d44eab7aa6e7ebce1b18ea6e74a61a371a9d49707cb0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull caddy@sha256:865d8c9990612444982aaf29f6fcb63cf6e70effa0f11839664031bf01cd5b85
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2881523201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14c21d5dee8e99eff212d3b500485558776bdb7dfa95bc5852f4324863a9c85`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Wed, 15 Dec 2021 00:45:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 00:45:53 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Dec 2021 00:45:54 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Dec 2021 00:45:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Dec 2021 00:45:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Dec 2021 00:48:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:48:32 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 00:50:15 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Dec 2021 01:12:34 GMT
ENV GOLANG_VERSION=1.17.5
# Wed, 15 Dec 2021 01:16:32 GMT
RUN $url = 'https://dl.google.com/go/go1.17.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '671faf99cd5d81cd7e40936c0a94363c64d654faa0148d2af4bbc262555620b9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 01:16:34 GMT
WORKDIR C:\go
# Wed, 15 Dec 2021 02:31:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 02:31:03 GMT
ENV XCADDY_VERSION=v0.2.0
# Wed, 15 Dec 2021 02:31:04 GMT
ENV CADDY_VERSION=v2.4.6
# Wed, 15 Dec 2021 02:31:05 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 Dec 2021 02:32:09 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 Dec 2021 02:32:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aabd70b2463e8240ac41c7d726f6fcfc25424b74f20bb5e8642dbb9bc2b789c8`  
		Last Modified: Wed, 15 Dec 2021 01:53:57 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a8639e414e28c147782b979f15c11cacfe3670dc5a898f9d0fc95ebadeb3f5a`  
		Last Modified: Wed, 15 Dec 2021 01:53:57 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a032d0c95307404bb3f5ccd3d69031082f2a3a1ab0eadd1ce3b12d931bd3e6`  
		Last Modified: Wed, 15 Dec 2021 01:53:54 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4ddbbfd5905588817615b135bf7431f7a67d054028d23d234b326a68097b39`  
		Last Modified: Wed, 15 Dec 2021 01:53:53 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22bfacbdbf128875fdbf7e39f4d3b2030fe3e310d9069f2a55924a2cf3e91ac`  
		Last Modified: Wed, 15 Dec 2021 01:53:53 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f566d739bb0bdf88e33c8c46b5751f6dcdf79a57d123fc0a559e3e189924cf4c`  
		Last Modified: Wed, 15 Dec 2021 01:54:00 GMT  
		Size: 25.5 MB (25463347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e73a67af47aee0d209f8dfd5ea371efb1b0c5205c8d5be95680c9675c302cb`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9036358af62e5d57f75caa56f99c1236c8bd7a61e2dd902f023c4ab45877aee`  
		Last Modified: Wed, 15 Dec 2021 01:53:51 GMT  
		Size: 341.0 KB (341030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc974df3fe45444aea125b83adabae2710ee41380c4942cf6e9f3ec314ad44ae`  
		Last Modified: Wed, 15 Dec 2021 01:58:00 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3bca46d6d1c61b00e6039bef7fb53bdbcb27e1a704241d9194c9ac7df77503`  
		Last Modified: Wed, 15 Dec 2021 01:58:30 GMT  
		Size: 145.4 MB (145421900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d466e52bb071b3ebbc307bf2043ee7c57e2dfe885c586bfdf6cc0e7d4068d851`  
		Last Modified: Wed, 15 Dec 2021 01:57:57 GMT  
		Size: 1.6 KB (1560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a39e48033de3f2e8d34e8175d6b1db65ac8dfba3ca370315d256e81ef7fc05`  
		Last Modified: Wed, 15 Dec 2021 02:35:23 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4b0296df5f5899cbda7155cbe412c7427b6f6c8013a44842b673348588b908`  
		Last Modified: Wed, 15 Dec 2021 02:35:20 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1655a91c512c917efab312f5008e8edfa31e1ac8dbc67099679df73afad4c132`  
		Last Modified: Wed, 15 Dec 2021 02:35:20 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d2b8fa77890c9b31b4c0768d5d4331a80812cc7cfb74810d962edf184f6c20`  
		Last Modified: Wed, 15 Dec 2021 02:35:20 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39569ad98a367d21e31f46b307003f5d2602c9b39cfb88288e4a302b29919dfe`  
		Last Modified: Wed, 15 Dec 2021 02:35:23 GMT  
		Size: 1.7 MB (1673776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69e84816c06da3d79b5a5528c8907c91a56f1aed658a56761ffa10b97f1e234e`  
		Last Modified: Wed, 15 Dec 2021 02:35:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
