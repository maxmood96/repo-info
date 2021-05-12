## `golang:1-windowsservercore-ltsc2016`

```console
$ docker pull golang@sha256:0aa0753d53526b5e8113cfc0135b6adb69483ce9375bda794cc2404c553c87bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4402; amd64

### `golang:1-windowsservercore-ltsc2016` - windows version 10.0.14393.4402; amd64

```console
$ docker pull golang@sha256:4cf4306987b8e39d1e4d9644621ba7ec37469ab6a5941ea0ae1c451a32d150b5
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5981426794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2291ca3296cc97edf8ec16607bcbc2909ebaff2328a370fd4166800c095163`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 26 Apr 2021 17:25:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 12 May 2021 12:29:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 May 2021 12:29:13 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 May 2021 12:29:14 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 May 2021 12:29:15 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 May 2021 12:29:16 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 May 2021 12:31:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 May 2021 12:31:45 GMT
ENV GOPATH=C:\gopath
# Wed, 12 May 2021 12:33:10 GMT
RUN $newPath = ('{0}\bin;C:\go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 May 2021 12:33:11 GMT
ENV GOLANG_VERSION=1.16.4
# Wed, 12 May 2021 12:37:08 GMT
RUN $url = 'https://dl.google.com/go/go1.16.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'd40139b7ade8a3008e3240a6f86fe8f899a9c465c917e11dac8758af216f5eb0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 May 2021 12:37:10 GMT
WORKDIR C:\gopath
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7f532f88613ca85064b055f6b93f8517bd05feba8fdce495a6ad1421573e765e`  
		Size: 1.7 GB (1725791397 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a280ee47051c0dfafc65e567f555ec59b7415288f965b44cf55c9187407d4248`  
		Last Modified: Wed, 12 May 2021 12:55:16 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10abf429e12c7b3b7d2b0a791d7cdb47866461a7b63df4ddd4f63acc91e26231`  
		Last Modified: Wed, 12 May 2021 12:55:13 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79955f676504cbf77ec284d8e857d18d17b93c5b8e6438b4062dd80f8632c9d6`  
		Last Modified: Wed, 12 May 2021 12:55:12 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24af485ecab19f81a0c65c0eaec6f6fda8749ca50eb53101abcfc5c079f9b1c2`  
		Last Modified: Wed, 12 May 2021 12:55:07 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b782f6bcd162ee81518d73c6c4fe5c5b731ab38b595c16a55ac185db84b2c9b`  
		Last Modified: Wed, 12 May 2021 12:55:07 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1327fc384f9fff64d41446adcb3bdf585307370ef0024a31a5269bae6f30067d`  
		Last Modified: Wed, 12 May 2021 12:55:18 GMT  
		Size: 30.8 MB (30797956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c50f4b0b5994b4154be9fea2ab6c6a0e4c402c44d44795a5ce82ab6f8de4bc`  
		Last Modified: Wed, 12 May 2021 12:55:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e458669a58e08411a0641a721ef1daf4af2a568c4dd61e9a3710b07f73b6ec`  
		Last Modified: Wed, 12 May 2021 12:55:13 GMT  
		Size: 5.7 MB (5661591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d753db33d9475a781a71db67226b6c2805f1e71108748b94dfdd610bb33137d`  
		Last Modified: Wed, 12 May 2021 12:55:04 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16cf5cfefdc254a6ea68d79ebf521696de46090dd4d38c207ff2e301ff621d2`  
		Last Modified: Wed, 12 May 2021 12:55:48 GMT  
		Size: 149.2 MB (149178430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8924854b0100f624a921d0d3d2922ca97fd7cca3d49cdc1dd677d10f628a122c`  
		Last Modified: Wed, 12 May 2021 12:55:04 GMT  
		Size: 1.5 KB (1543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
