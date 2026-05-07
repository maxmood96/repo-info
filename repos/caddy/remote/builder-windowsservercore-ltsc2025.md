## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:087b6423ac7d0c9d816958a61dabe23c54ff07e74fe62c6becb61c08ec8742fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull caddy@sha256:67e4b4ad0bdea2fb380b8e06ce8c50f3630268ce1398b04a26d216ee42162f28
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2253843447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a4efb84e5a47a774707f990e163d0329e80366d52ec7f6a049b4db66cc1de0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Thu, 07 May 2026 17:33:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 07 May 2026 17:33:54 GMT
ENV GIT_VERSION=2.48.1
# Thu, 07 May 2026 17:33:55 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 07 May 2026 17:33:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 07 May 2026 17:33:57 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 07 May 2026 17:35:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 07 May 2026 17:35:34 GMT
ENV GOPATH=C:\go
# Thu, 07 May 2026 17:35:40 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 07 May 2026 17:35:41 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:37:40 GMT
RUN $url = 'https://dl.google.com/go/go1.26.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '20d2ceafb4ed41b96b879010927b28bc92a5be57a7c1801ce365a9ca51d3224a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 07 May 2026 17:37:41 GMT
WORKDIR C:\go
# Thu, 07 May 2026 18:34:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 07 May 2026 18:34:14 GMT
ENV XCADDY_VERSION=v0.4.5
# Thu, 07 May 2026 18:34:14 GMT
ENV CADDY_VERSION=v2.11.2
# Thu, 07 May 2026 18:34:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 07 May 2026 18:35:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 07 May 2026 18:35:06 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401245195ad9ff7818f86e4b0155d19646f4196b024de2f44e5ee46ea742303c`  
		Last Modified: Thu, 07 May 2026 17:38:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2781522d52577d3a8415ef31f32cd927eb6cac7435ac05093589949d768cb810`  
		Last Modified: Thu, 07 May 2026 17:38:01 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f506d7ee63d3e4eb58f4cc2a06cd6baa5b5462a33859d5ffedc608093c13b6`  
		Last Modified: Thu, 07 May 2026 17:38:00 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f172078f3aa5c9044ad208f2f6a75e8879b8d40ff2b06e9336fcb583a5cae663`  
		Last Modified: Thu, 07 May 2026 17:38:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b37808e347a1b45df677699c031d7e12cf26360c8ba1f5295233c8857d26f7e`  
		Last Modified: Thu, 07 May 2026 17:37:59 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1342c05f6a9136a7d48d18c51c7d112b5c740957bcb152c380810efdff69a947`  
		Last Modified: Thu, 07 May 2026 17:38:06 GMT  
		Size: 51.3 MB (51270620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5434273a49508c5b8db2543533b0c91f5cda5e1d87e32edf95568706361261b`  
		Last Modified: Thu, 07 May 2026 17:37:58 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9108f6bccd5ec72456babe09793dd6c327ad82dbf58b4e737a1288b890760e8f`  
		Last Modified: Thu, 07 May 2026 17:37:58 GMT  
		Size: 350.0 KB (349953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73561c8b793b0afdffa3b3073417698a49712742ac11a1e74c5d6171a5864135`  
		Last Modified: Thu, 07 May 2026 17:37:58 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03fe8761e8f343c988495043b3ac2966f01b4b12a7e59dcee5cafd511951372`  
		Last Modified: Thu, 07 May 2026 17:38:09 GMT  
		Size: 69.9 MB (69892456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b815ad07a6727de1a666c0c6f250aeab5420d3e7101e09a891d4497628b0a8`  
		Last Modified: Thu, 07 May 2026 17:37:58 GMT  
		Size: 1.5 KB (1467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f4c1816fe4e416327b734a9a5661e7eb49de576a1745dbfe19197af02ff4e3`  
		Last Modified: Thu, 07 May 2026 18:35:17 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e5952958ae666ec7177b3fbb51c280f5368c3c1bce5880129bcf75496881f17`  
		Last Modified: Thu, 07 May 2026 18:35:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dfd713e840610597b7d36a00efc5e7f9a2ed45d92dfac6e4c7cb30ed7e4c0f`  
		Last Modified: Thu, 07 May 2026 18:35:15 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e18468816d2255812477ee302951c679087b1fcd5b6bc74c166c7da2e436b11`  
		Last Modified: Thu, 07 May 2026 18:35:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abce6cd161da6bf8b4aab48a5c1f115d91a1e5319dbb2ba4156530994b3761f`  
		Last Modified: Thu, 07 May 2026 18:35:16 GMT  
		Size: 2.3 MB (2327153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8244588779390cebb73002f912b0046d49747e2d1c94d16ab8bdfef293593d7a`  
		Last Modified: Thu, 07 May 2026 18:35:15 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
