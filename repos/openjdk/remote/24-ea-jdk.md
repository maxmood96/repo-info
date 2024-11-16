## `openjdk:24-ea-jdk`

```console
$ docker pull openjdk@sha256:dca2d72c921574315747dccda67c9fa1ff97768dd319ca354fab3bdfb375a76d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `openjdk:24-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:3eee0799644397d94d8b24e50c4b045f5a2b9fd025dffd63fb306af897526f7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **310.4 MB (310370619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c03ffcc26fb51bbd1a4d15127c4806982bb4c06aaa452a24bde00dccbae480`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 06 Nov 2024 16:23:18 GMT
ADD oraclelinux-9-slim-amd64-rootfs.tar.xz / # buildkit
# Wed, 06 Nov 2024 16:23:18 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1a9f94fc2db14421915984de2320d909c09c2f5b1d55a5a598eb1c60c59caf0`  
		Last Modified: Wed, 06 Nov 2024 20:17:02 GMT  
		Size: 49.2 MB (49218059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8faecf1dc429eb2f533abc3954faf4feb0d52697a438dee641a870f62d7d3e6c`  
		Last Modified: Fri, 15 Nov 2024 23:05:07 GMT  
		Size: 39.1 MB (39050410 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3311fb8191835db40810f9a06d08298302e92a0babc4433b781d94375b5b44dd`  
		Last Modified: Fri, 15 Nov 2024 23:05:11 GMT  
		Size: 222.1 MB (222102150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:4d524393cf2d69b5b9b5e30963864ad12bdab8395b065488781c364a7538ab90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3820060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64efbce0abb3e3a30b336e39cbe7159ad4fb4b1aeceb4342b37966da981151c7`

```dockerfile
```

-	Layers:
	-	`sha256:351be862e5539dcc4534860ce233f13951ed031cd70c63a846cb2aa31cde36ec`  
		Last Modified: Fri, 15 Nov 2024 23:05:06 GMT  
		Size: 3.8 MB (3800315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08714b3a55d94a711e00f02090b6dd014de2a67a838c77ba4748cde7b6142d09`  
		Last Modified: Fri, 15 Nov 2024 23:05:06 GMT  
		Size: 19.7 KB (19745 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:24c1647f2362b15c6883384717a3f9dcd2ac5009bd4c5db7bcb8720f622069c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307426191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b5432a60894d733c254931c248e484a81e9295ff4892656f540f1f370132fd`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 06 Nov 2024 16:24:10 GMT
ADD oraclelinux-9-slim-arm64v8-rootfs.tar.xz / # buildkit
# Wed, 06 Nov 2024 16:24:10 GMT
CMD ["/bin/bash"]
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-24
# Fri, 15 Nov 2024 01:48:14 GMT
ENV PATH=/usr/java/openjdk-24/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 15 Nov 2024 01:48:14 GMT
ENV LANG=C.UTF-8
# Fri, 15 Nov 2024 01:48:14 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 01:48:14 GMT
RUN set -eux; 		arch="$(rpm --query --queryformat='%{ARCH}' rpm)"; 	case "$arch" in 		'x86_64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='d6aa1bee11c9e9b14603f88fa1620ae6572d81194cf50a6d8da876ba2ff3ec40'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='1097eb5c1379e64a06ab8ba8a1af84a0802ab573823a7b8c792a5df8c1cc2509'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version # buildkit
# Fri, 15 Nov 2024 01:48:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d0164e3ac7ac3b1ed081f9b5c84a4e409b478d1e11a424210beaa96996e096d5`  
		Last Modified: Wed, 06 Nov 2024 20:07:55 GMT  
		Size: 47.9 MB (47891698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6462210e2d7b7d2ea30c30358ab0d739cc495b4de8d2eca0563575ff695ced2`  
		Last Modified: Wed, 06 Nov 2024 20:56:40 GMT  
		Size: 39.5 MB (39482424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:023cde86e525ed3962dc9e5c2e211b3b524b26c6d68199e525954641ab0ee4ba`  
		Last Modified: Fri, 15 Nov 2024 23:09:55 GMT  
		Size: 220.1 MB (220052069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `openjdk:24-ea-jdk` - unknown; unknown

```console
$ docker pull openjdk@sha256:bfa9babca8d0f4d0776246bdc727042f76500f6624fee1de00795473e26779ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 MB (3818106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd6fa2b7454cd0736e227fe91b271d94953d132f9d49a5cc39aa904cbee8a6a0`

```dockerfile
```

-	Layers:
	-	`sha256:3299112a65cc206b221a38061c0851557028643d91115fa7b46a74617b0c41ae`  
		Last Modified: Fri, 15 Nov 2024 23:09:51 GMT  
		Size: 3.8 MB (3798073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49ecf1fb3c7f56abfa1235e853f21a1ece009ecc00ad46132f9668259b326e27`  
		Last Modified: Fri, 15 Nov 2024 23:09:50 GMT  
		Size: 20.0 KB (20033 bytes)  
		MIME: application/vnd.in-toto+json

### `openjdk:24-ea-jdk` - windows version 10.0.20348.2849; amd64

```console
$ docker pull openjdk@sha256:540a0fa22fef3c0543666997ecb243b0dae0c40d2a64b49eac13d821b2687094
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471200411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e1920f5260a9b238a22f47f75906a9193c1fd7e51a7b660e210f0f82d19d6a1`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Fri, 15 Nov 2024 23:11:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 Nov 2024 23:11:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:11:42 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 15 Nov 2024 23:11:47 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:11:48 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 23:11:48 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_windows-x64_bin.zip
# Fri, 15 Nov 2024 23:11:49 GMT
ENV JAVA_SHA256=403403eb4a5860551cdfc63a2395f87cf7526bf93e5437ea5fd17168572fd51a
# Fri, 15 Nov 2024 23:12:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:12:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a50bfc4a6c23d4423657c38fd801af499a6f07385aac6bc4de89349efd74a5`  
		Last Modified: Fri, 15 Nov 2024 23:12:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8685fed0880fa63804a38da03e6726d5b87af3470b1000e3850658442ab163e`  
		Last Modified: Fri, 15 Nov 2024 23:12:15 GMT  
		Size: 361.4 KB (361396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c9f9952eb61cfe35b6ae63510d1a3eec4a1d973df226f2c33bee7ab7092757`  
		Last Modified: Fri, 15 Nov 2024 23:12:15 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3fe30b86acfebbf39c2a385395a465e1e1d746e47d944d371d26ec4c30c7106`  
		Last Modified: Fri, 15 Nov 2024 23:12:18 GMT  
		Size: 345.7 KB (345748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682f1a38d4f3e90d9ac6c98b9c0dad114fb26e7c2d7a885e98ef022e082454a3`  
		Last Modified: Fri, 15 Nov 2024 23:12:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1abf23c2a71e46129f71f9a9664a231f487fb970025a12ccecb5ba4b0430c64`  
		Last Modified: Fri, 15 Nov 2024 23:12:13 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e87fc0af2adb498a0fbc6ee6bb959c19304a8024a288a8cd66d770cb570cb`  
		Last Modified: Fri, 15 Nov 2024 23:12:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb30d1730e4e5ca26d22cd14fb78e8e03b9a19aee06c79f3b0bf84da0626ae87`  
		Last Modified: Fri, 15 Nov 2024 23:12:25 GMT  
		Size: 218.0 MB (218001331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b233d0f611de1e1f888f8bfed8ae55ea1615011ee9f38e58cdcd6a370fdf1b94`  
		Last Modified: Fri, 15 Nov 2024 23:12:13 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:24-ea-jdk` - windows version 10.0.17763.6532; amd64

```console
$ docker pull openjdk@sha256:38419d99f190430797c994d1786a4343b11c2969002df108f53b8614e27864cb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229502792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ace56a105bc37f3eb07f562006c5fd29219b0cce3dd2979f6b7d86fd18e2e13`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Fri, 15 Nov 2024 23:04:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 Nov 2024 23:06:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:06:02 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 15 Nov 2024 23:06:21 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:06:22 GMT
ENV JAVA_VERSION=24-ea+24
# Fri, 15 Nov 2024 23:06:22 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/24/GPL/openjdk-24-ea+24_windows-x64_bin.zip
# Fri, 15 Nov 2024 23:06:23 GMT
ENV JAVA_SHA256=403403eb4a5860551cdfc63a2395f87cf7526bf93e5437ea5fd17168572fd51a
# Fri, 15 Nov 2024 23:06:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 15 Nov 2024 23:06:59 GMT
CMD ["jshell"]
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
	-	`sha256:4fecedf989bf78ec7c563a5ce533ea5ef3405e8bc70347dc2eea9d25aaf49745`  
		Last Modified: Fri, 15 Nov 2024 23:07:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e9abf92dcbe4382036e597ce2e628ce6c0f83f89f11fb56cd2db409d3b9e2d`  
		Last Modified: Fri, 15 Nov 2024 23:07:06 GMT  
		Size: 494.0 KB (493953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b83b95abb262cd2d7bd8c41d7d00e1ed1f139426745f5c87ca2091deeb0a8cb`  
		Last Modified: Fri, 15 Nov 2024 23:07:06 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c24d4b751569e580e4b4664d55c2401d570ece3c34082d12b6b51909f3c21bc`  
		Last Modified: Fri, 15 Nov 2024 23:07:06 GMT  
		Size: 338.0 KB (338005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:badb0c837ee95f21c0a134239fc9f84edebf442e21229898b6260c506751407f`  
		Last Modified: Fri, 15 Nov 2024 23:07:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ce007f8d8872b22925529b05d016855bac4d3ec9467b943836cf703ad85b356`  
		Last Modified: Fri, 15 Nov 2024 23:07:04 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7768931be92a708c019f1bf47eb1abd848ee96f378f054423088ee1f2fc4ee`  
		Last Modified: Fri, 15 Nov 2024 23:07:04 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60e7c9e03dba687f180ed9e9263107b1db1dfcbb51f9dcc0282d7f3c981e9ab`  
		Last Modified: Fri, 15 Nov 2024 23:07:17 GMT  
		Size: 218.0 MB (218009268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323ec0c8fcde3b8c2ab2eda3de192884cd0f93d712e80665fcc4035aacc60394`  
		Last Modified: Fri, 15 Nov 2024 23:07:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
