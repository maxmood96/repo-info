## `openjdk:19-jdk`

```console
$ docker pull openjdk@sha256:71100a7c44df218034bbea507b23ad528c3b2925c359b9f42a2c802b0156b607
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `openjdk:19-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:c498198ed516a526b4906178d35c8a2cc922cede42aa119cc0bc62b3d864b974
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.8 MB (245755748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e21544a77f5f9c87eeb203b8b6307b21db0102a523114df8a5da063ee5470542`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Feb 2022 05:30:31 GMT
ADD file:17957b69b27e30b1d860c0919546da181b5e126b4aca4e1935ab44fd1832578e in / 
# Fri, 04 Feb 2022 05:30:31 GMT
CMD ["/bin/bash"]
# Fri, 04 Feb 2022 06:31:47 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 08 Feb 2022 03:42:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 08 Feb 2022 03:42:29 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Feb 2022 03:42:29 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 03:42:29 GMT
ENV JAVA_VERSION=19-ea+8
# Tue, 08 Feb 2022 03:42:43 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='64f85aad4da5d214002ccbf442b38618b6fae689e66fec2f4a52253d1654683c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='55bc6f3f3db8a59c77e43ee8ee1ea99d3f121b48d3c7d54cf84f2660a008f047'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 03:42:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f431a76c5f59c48efd4a4076677acaae2b540a7562de00075162ef8a340fd69b`  
		Last Modified: Fri, 04 Feb 2022 05:31:30 GMT  
		Size: 42.1 MB (42102405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0509e57e85d3b85eac03c20f8f88d1cb2481d6122bdae0020851f7022e3b31`  
		Last Modified: Fri, 04 Feb 2022 08:22:45 GMT  
		Size: 13.5 MB (13513973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432790937fac54eb0d642ffbc9e27470b31f127d3889d6810f54056133b337e2`  
		Last Modified: Tue, 08 Feb 2022 03:53:28 GMT  
		Size: 190.1 MB (190139370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:3d228fd87074b53dfdf45168508149d0b8c868e8b7e9beb751ae2d64aa53b213
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.5 MB (245480295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3aab256b620b45982ac26aeb6ba2b14cf0df92c5d931f5903ff977b40b48b44`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Feb 2022 04:13:53 GMT
ADD file:22ac13d97f9f75668fec05f2cf9d182e5edcf2822b08ef38929b0bb8d61f5edb in / 
# Fri, 04 Feb 2022 04:13:54 GMT
CMD ["/bin/bash"]
# Fri, 04 Feb 2022 05:34:11 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Tue, 08 Feb 2022 06:23:11 GMT
ENV JAVA_HOME=/usr/java/openjdk-19
# Tue, 08 Feb 2022 06:23:12 GMT
ENV PATH=/usr/java/openjdk-19/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Feb 2022 06:23:13 GMT
ENV LANG=C.UTF-8
# Tue, 08 Feb 2022 06:23:14 GMT
ENV JAVA_VERSION=19-ea+8
# Tue, 08 Feb 2022 06:23:36 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_linux-x64_bin.tar.gz'; 			downloadSha256='64f85aad4da5d214002ccbf442b38618b6fae689e66fec2f4a52253d1654683c'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_linux-aarch64_bin.tar.gz'; 			downloadSha256='55bc6f3f3db8a59c77e43ee8ee1ea99d3f121b48d3c7d54cf84f2660a008f047'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Tue, 08 Feb 2022 06:23:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:200ed4b56d545919e183ba8dfa2493452065262be1759dd78c3de721a71882cb`  
		Last Modified: Fri, 04 Feb 2022 04:14:59 GMT  
		Size: 42.0 MB (42011648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4545cbf19e4d384cf8f28f10cdb2cb3e0cfb6a09f47542c1c092358c7fd1b5`  
		Last Modified: Fri, 04 Feb 2022 05:50:37 GMT  
		Size: 14.3 MB (14290526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5ac9153308221b4ea772e76262649172393eedbbedf91d2fdc59a4c9d4471`  
		Last Modified: Tue, 08 Feb 2022 08:19:38 GMT  
		Size: 189.2 MB (189178121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - windows version 10.0.20348.473; amd64

```console
$ docker pull openjdk@sha256:97fe8267bceb2ddd878422990784a0e6eb79d753795e976ec4cffc196ae8c86d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2394095378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8fc775a94a5506aa73bc9cf432f89c6f763d19289d8a6d7df25e485871c76c7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Sun, 16 Jan 2022 05:17:24 GMT
RUN Install update ltsc2022-amd64
# Wed, 19 Jan 2022 22:21:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 22:23:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 22:23:13 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 22:23:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:16:01 GMT
ENV JAVA_VERSION=19-ea+8
# Tue, 08 Feb 2022 02:16:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_windows-x64_bin.zip
# Tue, 08 Feb 2022 02:16:04 GMT
ENV JAVA_SHA256=eba519024733a2420e4c45145f4995121a1612f2dc875c1d37b0b87b69d563c2
# Tue, 08 Feb 2022 02:17:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:17:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0e02c12b1310e6c76c29fcd6f81905400fdb6a01caac9dc825939ad004baffef`  
		Size: 955.8 MB (955800778 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2e1f45a873642f0aab3474828d75469362741244e7c714068ac1afe056102cd6`  
		Last Modified: Thu, 20 Jan 2022 00:40:19 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa436893917b4b24f7020ae30c97fa33ab983d9c24e6fd7534d56f8b19bf786f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 601.2 KB (601200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039cc436f8de7b22962fef11f63ff7fb05b1dad02d0b04d62c514a24ef045cf9`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:880009a6e2005dbfbbe934f1896114d21a0e91c8bdaffaee2d5349c8e9de467f`  
		Last Modified: Thu, 20 Jan 2022 02:19:54 GMT  
		Size: 506.3 KB (506304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230bc8140a00773d1f98d4eb9740fdabf77c4a0e627411866f93c2bcf5fe44ba`  
		Last Modified: Tue, 08 Feb 2022 03:20:57 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcec6c117ceb6c768b0bd07254fe6340382589d2060e8847d99c4d495295872`  
		Last Modified: Tue, 08 Feb 2022 03:20:57 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9ac597910dd57dc269873625a983522abb78bd613c2b0e22e672f726e54bb2c`  
		Last Modified: Tue, 08 Feb 2022 03:20:57 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fce07c0e9c2a1d8e7157af7537405e923e44e50a8f0658a8784fca5634c9ba9`  
		Last Modified: Tue, 08 Feb 2022 03:24:21 GMT  
		Size: 185.5 MB (185479512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc1b5d167fec337d8d7f7432a817b9bb184eda685bae5066ca8acb4a6558912`  
		Last Modified: Tue, 08 Feb 2022 03:20:57 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:19-jdk` - windows version 10.0.17763.2458; amd64

```console
$ docker pull openjdk@sha256:cacead43cc807629b0e5ea15cb5a1b0a74837914d5014284df724d1ede89a834
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2899295796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d37073ef28e2daad42e78124740f491af4d8f68d57bf54cbeaebae8f6aa255da`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 18 Jan 2022 01:52:23 GMT
RUN Install update 1809-amd64
# Wed, 19 Jan 2022 23:21:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 19 Jan 2022 23:23:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 19 Jan 2022 23:23:42 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 19 Jan 2022 23:24:43 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:17:44 GMT
ENV JAVA_VERSION=19-ea+8
# Tue, 08 Feb 2022 02:17:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk19/8/GPL/openjdk-19-ea+8_windows-x64_bin.zip
# Tue, 08 Feb 2022 02:17:46 GMT
ENV JAVA_SHA256=eba519024733a2420e4c45145f4995121a1612f2dc875c1d37b0b87b69d563c2
# Tue, 08 Feb 2022 02:19:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 08 Feb 2022 02:19:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:567fd00846e9a9f44eea5925b497356dda00fe89b8335d2a3b2a8b9d84b0bb69`  
		Size: 995.0 MB (994988595 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ba7b1090ce9545f6aac90d390785f6c5e3846304cb7596289dfc36c169d7b1da`  
		Last Modified: Thu, 20 Jan 2022 00:40:41 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a98c73c8d54eeae51e9c93499966b4413ea63f218bdf175bed7b7d83c76e6d58`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 357.3 KB (357347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64554bb59fd3345200ae4e79426f465295d19e9d1be31e0f5a60f5ddc13af5b2`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec53942b6c9dd8e8c55c8a2268d1a09a715d75e3edcf063826fa7462dcdb7c2`  
		Last Modified: Thu, 20 Jan 2022 02:20:37 GMT  
		Size: 310.5 KB (310471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb93382399dbf19897266c16425c40ec4bef7b27f3687373cb3221e8ae0d2c13`  
		Last Modified: Tue, 08 Feb 2022 03:24:42 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0825b2736c6f8d9e43eabd301cf7658b87ba942d59cf0352d35aa753b43bb8f7`  
		Last Modified: Tue, 08 Feb 2022 03:24:42 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da30a4a85393397b050a1f427f830ea9c9af09508b82c05fde395ac3358e76a5`  
		Last Modified: Tue, 08 Feb 2022 03:24:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f5a55378c92d153ee53021f7a1ad85250278a448407d8777e0b901cb768162`  
		Last Modified: Tue, 08 Feb 2022 03:27:56 GMT  
		Size: 185.3 MB (185297980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eeba1d031806eed5264fb70e38b9ed8eddbe6d21f13fa6f872e84994abb4118`  
		Last Modified: Tue, 08 Feb 2022 03:24:42 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
