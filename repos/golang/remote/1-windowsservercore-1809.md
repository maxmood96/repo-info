## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:204712f534c125e4eace999c1a26e9300a3f70f9a379ae04fbf8f984661886d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull golang@sha256:88c1a0bdbeda0814408ed852950f7745ed0e9a9a97b9ad1651d4976fc1b0c5e0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2113953772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99b8cffce73aef5e324adb631b7bd00af9946a9e68faa4b8365039e4c7d2e81b`
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
