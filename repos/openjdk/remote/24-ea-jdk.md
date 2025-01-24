## `openjdk:24-ea-jdk`

```console
$ docker pull openjdk@sha256:c5e32b1841ccbe3ab101c321a1848897b31faf2d81b01679e3e0162f834e4d72
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:a9fdc8c6f7dae834c6be52f9db3af529c7c96df27d9f24d453e639910ad49549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.6 MB (310649663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:671d2909c605cbb15a8dac9d1f9fc529b07a6b39bd5858a695d3ace775bc1c0b`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:42:52 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:42:52 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2c0a233485c3a7b6cab556a9a9c2916ca9a3afc8c46097ddfbe0af4fe120a50c`  
		Last Modified: Thu, 21 Nov 2024 22:26:24 GMT  
		Size: 49.1 MB (49098702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce868e6ebff65cd828251ad179b6c0a331ec470c760695923c4bc38397f7d60e`  
		Last Modified: Thu, 23 Jan 2025 22:27:09 GMT  
		Size: 48.8 MB (48774984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758c4b779b9233353ddef6faaa1d76d82fb3cf05dfb91c46730ddacaa1ca0bfd`  
		Last Modified: Thu, 23 Jan 2025 22:27:11 GMT  
		Size: 212.8 MB (212775977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:dfdeaea7ab1fcd99251e54617702cfc5dfb5b2a3b5cbd9d1e7efc815bfb36517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4927321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68357f61198ced074c0a289db64a3aedc3ee74688cdd0859901e92cff64494f4`

```dockerfile
```

-	Layers:
	-	`sha256:fd09a121c09abf05f432c878c2bad2ea40739a00b88fe244a2e871de38f61fbd`  
		Last Modified: Thu, 23 Jan 2025 22:27:08 GMT  
		Size: 4.9 MB (4907575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65e36fa64090994ea8b614b2268605f53316f7d051094288a672d0bb0de0ec75`  
		Last Modified: Thu, 23 Jan 2025 22:27:08 GMT  
		Size: 19.7 KB (19746 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:710cbbb73c87615e4116b4925c2bfcc4a8c743841009986d50c4731843bdb4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.6 MB (307600151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5027a8fe98120fedd58fbce396eeebbd04f7e0e624a83090f150e13f9f34b4a8`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 21 Nov 2024 19:43:03 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Thu, 21 Nov 2024 19:43:03 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Thu, 23 Jan 2025 19:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2025 19:48:14 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 19:48:14 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 19:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-x64_bin.tar.gz'; 			downloadSha256='52afbfd5229250d1a724367cda6380f2acff08c58ee9bfcc6db727ccf4feb251'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_linux-aarch64_bin.tar.gz'; 			downloadSha256='4c6890d8da82bc38820c3b8330579c9083a6dbc834c5026def54e9b83bc18dbe'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Thu, 23 Jan 2025 19:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f7fa64c7935f6bb5df09447a656c51d0f8f2a9f6c57838b88508dce34d5ec36a`  
		Last Modified: Fri, 22 Nov 2024 04:12:55 GMT  
		Size: 47.7 MB (47667392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9527a70a5df0c50a0919b2bbc807b6789f8d6833d49f997079d3ab5dd2e735`  
		Last Modified: Wed, 22 Jan 2025 02:29:30 GMT  
		Size: 49.2 MB (49203729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1044ee2c4fb15e6dcfeeb709b8d122b4f848d38788d91fb9a757c3c4d6a2945`  
		Last Modified: Thu, 23 Jan 2025 22:29:55 GMT  
		Size: 210.7 MB (210729030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:f3871df0c7f960ee8f64e941ea49b282305c0288c8a5dc156bc3c17838437097
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4925370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ad9a7570c71de645bf6f7a13eba0816ee81ba32c1df3eefbbafb5b2e7faf84`

```dockerfile
```

-	Layers:
	-	`sha256:776bc2f84dbc0ce4a0ceca1eb193e21883ca1bc7f24674cf9fe471f02f90ab4e`  
		Last Modified: Thu, 23 Jan 2025 22:29:49 GMT  
		Size: 4.9 MB (4905337 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60e74bb7f6a63d78ce585df0b61a52a6d8992969b11cafe0a1dbbe97168e0e6`  
		Last Modified: Thu, 23 Jan 2025 22:29:48 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk` - windows version 10.0.26100.2894; amd64

```console
$ docker pull openjdk@sha256:2af2b4d23bd8699ba40cafa900bbcd11415f14ad46cf5c2dd83480cb78eefca8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2709970676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46a9d8fd55b50baa1d61f3d6c490edb039f0bdf652e305734faa3524ab506167`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Thu, 23 Jan 2025 22:29:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:29:58 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:29:59 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 22:30:05 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:06 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 22:30:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_windows-x64_bin.zip
# Thu, 23 Jan 2025 22:30:07 GMT
ENV JAVA_SHA256=e5f13b2b408e1c98310b5fac3025ff52a576a8ca77ad40ec8a1e90d8d1ca3094
# Thu, 23 Jan 2025 22:30:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:30:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d31051af3441fff8ceffe0d7d229bf6e16c93fe8249510aa7f14ab1c3da146`  
		Last Modified: Thu, 23 Jan 2025 22:30:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ace684bc0a5a15ffdea29c2135185762630057b05c52fcbec37a2503ae02862`  
		Last Modified: Thu, 23 Jan 2025 22:30:33 GMT  
		Size: 395.3 KB (395330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec84ca491f6f2aeef424ec1a638fa1ecec9b9a906132c6c5e88e446b5463446`  
		Last Modified: Thu, 23 Jan 2025 22:30:32 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffb09f553c2927b00078f8719ae798bab69a8461167ee360659363de6b85ae8`  
		Last Modified: Thu, 23 Jan 2025 22:30:32 GMT  
		Size: 383.0 KB (383045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d8d3ed832ef393390b14922c9f1c04dcedfc46ae34c717423f431964922ddb`  
		Last Modified: Thu, 23 Jan 2025 22:30:30 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b939e082500da86767bf0932f010d338880b23e9484103ff4e7c05a24f1e1e8d`  
		Last Modified: Thu, 23 Jan 2025 22:30:30 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bca0d37e61c9e1fcd62870bc1ffb1f1cb4692474d3c9d10724b734f405d3a31`  
		Last Modified: Thu, 23 Jan 2025 22:30:30 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6796d6f4ffb8f1caa42b408e494a5c5170d39b07d89b3a7bdde41f6738510674`  
		Last Modified: Thu, 23 Jan 2025 22:30:42 GMT  
		Size: 208.9 MB (208906925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef12dae2f1420cf78617dac6f90a0807b31399ff416986c33a46c6f2627f55f`  
		Last Modified: Thu, 23 Jan 2025 22:30:30 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-jdk` - windows version 10.0.20348.3091; amd64

```console
$ docker pull openjdk@sha256:30c49f275496565c03f96165c450159c8b33e9faa163fb214f88f063c5b2a487
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471905571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d25f5b5a9a665d43e9b0bb2dec10b0c6d9ac747319783f3f5ff56c95d69f99`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Thu, 23 Jan 2025 22:26:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:27:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:19 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 22:27:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:26 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 22:27:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_windows-x64_bin.zip
# Thu, 23 Jan 2025 22:27:27 GMT
ENV JAVA_SHA256=e5f13b2b408e1c98310b5fac3025ff52a576a8ca77ad40ec8a1e90d8d1ca3094
# Thu, 23 Jan 2025 22:27:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:27:56 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ea6003db03061d3996c029df04bb835460717c2dabb7bd287c115a17d3e8c5`  
		Last Modified: Thu, 23 Jan 2025 22:28:03 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf95d4f2bd025d92d79f37b2a178c04622f000efc7420ca79cef7498ac6c1d46`  
		Last Modified: Thu, 23 Jan 2025 22:28:03 GMT  
		Size: 363.8 KB (363775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4660a9e5ccae9aa2392986bed7cb60ec31cba0cda82aca9f1e9c368e23bee3b9`  
		Last Modified: Thu, 23 Jan 2025 22:28:03 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619b5659bba8b428e4054bb0872c141f46768cfff6d02e9ae06ad4fa05339ca8`  
		Last Modified: Thu, 23 Jan 2025 22:28:03 GMT  
		Size: 311.7 KB (311660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc40dbbcb3c467f890431a435df9803a643c1e08fb46c31a21884625c23222c`  
		Last Modified: Thu, 23 Jan 2025 22:28:01 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb4eacc5442b5cdd77d458d2a5a2d8cf0b8a186414f0e34735ae471567ce1d32`  
		Last Modified: Thu, 23 Jan 2025 22:28:01 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee524de7e1ddb8e06394cb972176922950cdb13007eeb5be95b83b002534a78`  
		Last Modified: Thu, 23 Jan 2025 22:28:01 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d56599663954a41f18cffefff7544d586e111524f76c06d77736730c80d4f0`  
		Last Modified: Thu, 23 Jan 2025 22:28:12 GMT  
		Size: 208.8 MB (208836797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b50758e849d2ea3ed166b768c3da16c07ee6ef79a9030e18daab4e66c70849dc`  
		Last Modified: Thu, 23 Jan 2025 22:28:01 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-jdk` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:32d7cb48e87a6210b8db34fe05e98f03daca56ab21686a4f70c10f399d2631b8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331753827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc462c140d4dc9449837b2e88ec28e12e3a30612b8c8476377877233f121bd7a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 22:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:28:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:09 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 22:28:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:19 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 22:28:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_windows-x64_bin.zip
# Thu, 23 Jan 2025 22:28:20 GMT
ENV JAVA_SHA256=e5f13b2b408e1c98310b5fac3025ff52a576a8ca77ad40ec8a1e90d8d1ca3094
# Thu, 23 Jan 2025 22:28:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:29:00 GMT
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
	-	`sha256:3fbb6c7809faf79f45e23fc488e33706477f780769406b3106d23357077f067f`  
		Last Modified: Thu, 23 Jan 2025 22:29:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4b929e4dab1a122d348aa4f3c4d0092f4fd70243ea211b281e586e5c58346c`  
		Last Modified: Thu, 23 Jan 2025 22:29:07 GMT  
		Size: 340.8 KB (340761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b02ecaf0494301ef1e9530dea35e7e09dda72b87ec20a0bc1983cc01cafe2`  
		Last Modified: Thu, 23 Jan 2025 22:29:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c897560bc646820cbfc297b6c8efc67dd75c87058c5c3468e94b178883119a8`  
		Last Modified: Thu, 23 Jan 2025 22:29:07 GMT  
		Size: 331.2 KB (331164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e8d53eeac021cec00f2b244dc11c89db3b3865311c8419e3d2ccff818d8c2`  
		Last Modified: Thu, 23 Jan 2025 22:29:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129807b7a42cd8ace2168a47bc666b1aaa922fab8694c4ea3c45f9950866722f`  
		Last Modified: Thu, 23 Jan 2025 22:29:05 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a3f350f71ecbaec116a8832c004d363e376befcb8cd46ddee0bda5be1d9558`  
		Last Modified: Thu, 23 Jan 2025 22:29:05 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f12864af61bff541919258a0f8bfdeb5fbba115ab25384828535d9fb3d2a871`  
		Last Modified: Thu, 23 Jan 2025 22:29:16 GMT  
		Size: 208.9 MB (208861857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02772b89adebe158575d790638b54d65fbf6db4ad463e69a9feb24fc469c3a22`  
		Last Modified: Thu, 23 Jan 2025 22:29:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
