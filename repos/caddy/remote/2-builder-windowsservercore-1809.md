## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:2c1ed06c892c00c3264c24308dbb307712f0015c5eb4349c455bffcb7aeea5d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull caddy@sha256:6d491753b513340f409224526e01149f43fca654c2677d94a4d3371d91d0cbdb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2116271015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b066319a9378683d7a63e9b0da44c135803a7a874ca11f8316fd189cc0996a6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:23:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:23:51 GMT
ENV GIT_VERSION=2.23.0
# Thu, 14 Nov 2024 20:23:51 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 14 Nov 2024 20:23:52 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 14 Nov 2024 20:23:52 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 14 Nov 2024 20:24:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:24:57 GMT
ENV GOPATH=C:\go
# Thu, 14 Nov 2024 20:25:03 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Nov 2024 20:25:03 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 14 Nov 2024 20:26:50 GMT
RUN $url = 'https://dl.google.com/go/go1.23.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '81968b563642096b8a7521171e2be6e77ff6f44032f7493b7bdec9d33f44f31d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:26:51 GMT
WORKDIR C:\go
# Thu, 14 Nov 2024 21:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:11:58 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 14 Nov 2024 21:11:58 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 14 Nov 2024 21:11:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 14 Nov 2024 21:12:18 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 14 Nov 2024 21:12:19 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d52f4c013c77270259a2f26570ebb97024133f39e5f0d0d19bd21fd1d1796e6`  
		Last Modified: Thu, 14 Nov 2024 20:26:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3489509c6b25c07ceb11893b75bde11cf7c7b819674bdc97234f73bb3ff0ae7`  
		Last Modified: Thu, 14 Nov 2024 20:26:56 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715e1895f4e13c156164e502d11014398c76a8f9dd8636a3855ae21bf04e1a95`  
		Last Modified: Thu, 14 Nov 2024 20:26:55 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c2bbcafc8c9f05fdaecff0555bc092b7e0461e80478bf63950ae7784a89b780`  
		Last Modified: Thu, 14 Nov 2024 20:26:55 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874b8db3d7c4c5af75f7032d17e668c06dac0de0594b07904de11ee5bae7f530`  
		Last Modified: Thu, 14 Nov 2024 20:26:55 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64df1cbde32408f8c5df6b4503cc5b073e33da80975ae4b3cb9ec52fb3a0b9bb`  
		Last Modified: Thu, 14 Nov 2024 20:26:58 GMT  
		Size: 25.6 MB (25595821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997ffdbcaacba4dba95391b8b8969bb9fce2730508cc3becf801317e9d156af8`  
		Last Modified: Thu, 14 Nov 2024 20:26:54 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f8dcc61e95c50185b9fce6d34bef8fbea61a1a94ab559e124bc3f40319dd2c2`  
		Last Modified: Thu, 14 Nov 2024 20:26:54 GMT  
		Size: 350.5 KB (350480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba863396492f1dd427318fd428534b657c92c328ffd927fe49edf1acf78b5589`  
		Last Modified: Thu, 14 Nov 2024 20:26:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99cc7e08b3db3451f8a6a9f6ca0c75462003691d4398f66739233026febb413a`  
		Last Modified: Thu, 14 Nov 2024 20:27:06 GMT  
		Size: 77.3 MB (77343118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4013366b353c80d248772e41afb787ff69271bef3e0dbb4735f0bcc3a865ac5f`  
		Last Modified: Thu, 14 Nov 2024 20:26:54 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62bb6c5d504da39e79084aca36201beecd8a0b546d46a392d9f3c42f3d65298`  
		Last Modified: Thu, 14 Nov 2024 21:12:25 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcebeabade58313305d1d624f33f47c9aa28acaa72d86935182a4c2df7714a15`  
		Last Modified: Thu, 14 Nov 2024 21:12:23 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d7dc7a2871df9cc1884f4334ad35a49c5d24642fbba451ae5ec2c284078a06`  
		Last Modified: Thu, 14 Nov 2024 21:12:23 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb1454f671596ae84b8a49b7e5fc2a56b572606b220d92ad854ebf91963dc01`  
		Last Modified: Thu, 14 Nov 2024 21:12:23 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed6cef4b227bcbf85297f3f516e98d0e5fdbaec61b4841371bb4acda4ae8327`  
		Last Modified: Thu, 14 Nov 2024 21:12:23 GMT  
		Size: 2.3 MB (2310462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2661cff6c74e6dfe14876c0a70072ecc519dd1ee51b90cb6e662d6492b65aab`  
		Last Modified: Thu, 14 Nov 2024 21:12:23 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
