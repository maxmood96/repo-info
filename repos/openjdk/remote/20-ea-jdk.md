## `openjdk:20-ea-jdk`

```console
$ docker pull openjdk@sha256:960b9e84d951d685ed29cd85be9db35b1d0c677ae98b77f788ed69c16fefb5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	windows version 10.0.20348.1006; amd64
	-	windows version 10.0.17763.3406; amd64

### `openjdk:20-ea-jdk` - linux; amd64

```console
$ docker pull openjdk@sha256:76d5e0763505110083e0cbf9edc8c49a603cf34f289b0804f982f09613251263
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **249.7 MB (249715233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca95b560ae0bb2583667e7db48fa5dafbef493f96c84ba51aad5cd3596e2449`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Sep 2022 21:20:28 GMT
ADD file:e00d9d8d8f616feec8c064f2250e4836ea3b533ead0611d1af2245974abb4e88 in / 
# Wed, 14 Sep 2022 21:20:28 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 21:37:14 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 14 Sep 2022 21:37:14 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 14 Sep 2022 21:37:14 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Sep 2022 21:37:14 GMT
ENV LANG=C.UTF-8
# Fri, 30 Sep 2022 23:30:03 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:30:14 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9d46acb0892a134f62ab21fca33fdef1da5d579f61ddbd0ae3ff0b4d33c5eca2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='31245b15195bf9f12a6db08474bfcbd1ddbccc76436372bf4db538c6ede8f976'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 30 Sep 2022 23:30:14 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:051f419db9dd9462e8995886d24f592c26cef792cc915dfbc7548e0b19aa55fe`  
		Last Modified: Wed, 14 Sep 2022 21:21:25 GMT  
		Size: 40.6 MB (40590248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa51c6010a14c1984cbdea1332a5d2f77bf6e0141bc497b44dca611e21f9b391`  
		Last Modified: Wed, 14 Sep 2022 21:41:16 GMT  
		Size: 12.2 MB (12232427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade728927a3fe29651eddb2dc4af5ec23a96c27ecdf3cd3fc8d42d02b1439084`  
		Last Modified: Fri, 30 Sep 2022 23:34:13 GMT  
		Size: 196.9 MB (196892558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk` - linux; arm64 variant v8

```console
$ docker pull openjdk@sha256:cd1d15290753bd7f25bb7ea0bb8f02e68042134054585e1448837bf0c6d1d605
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.9 MB (247924188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547612219d79c6f2357beef1f3539e0f52a4e58fd5902874cd51fa30702c9ad7`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 14 Sep 2022 21:41:16 GMT
ADD file:30401488699aa4b911abaeec83f0938e0fede937c09940369ec58cc56eae4624 in / 
# Wed, 14 Sep 2022 21:41:17 GMT
CMD ["/bin/bash"]
# Wed, 14 Sep 2022 22:01:28 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 14 Sep 2022 22:01:28 GMT
ENV JAVA_HOME=/usr/java/openjdk-20
# Wed, 14 Sep 2022 22:01:29 GMT
ENV PATH=/usr/java/openjdk-20/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Sep 2022 22:01:30 GMT
ENV LANG=C.UTF-8
# Fri, 30 Sep 2022 23:25:45 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:27:08 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-x64_bin.tar.gz'; 			downloadSha256='9d46acb0892a134f62ab21fca33fdef1da5d579f61ddbd0ae3ff0b4d33c5eca2'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_linux-aarch64_bin.tar.gz'; 			downloadSha256='31245b15195bf9f12a6db08474bfcbd1ddbccc76436372bf4db538c6ede8f976'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 30 Sep 2022 23:27:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9a8b791677e1fdf76ff862b55362355b48c8636d0eabf606d1af65888ab73ec8`  
		Last Modified: Wed, 14 Sep 2022 21:42:22 GMT  
		Size: 39.4 MB (39409909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1458b25adde8441e97a5f07c35975478bc0d77410ada29b87b31f52fbbaf994`  
		Last Modified: Wed, 14 Sep 2022 22:09:27 GMT  
		Size: 13.1 MB (13055052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b67770e3410f1755266f2a3ffc6c5385f24be15cba615fc1d9a254f64718bd`  
		Last Modified: Fri, 30 Sep 2022 23:34:22 GMT  
		Size: 195.5 MB (195459227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk` - windows version 10.0.20348.1006; amd64

```console
$ docker pull openjdk@sha256:4ed78ee31756e0f8d488d4f3ac311d6303537f776acc574fa41930efa8c8f293
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2540509155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27de124f0a76c8109c0cfe63fe17ea33147317adc7615e1de436e3f8b3cfc6c7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 17:03:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Sep 2022 17:03:53 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Sep 2022 17:04:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 Sep 2022 23:23:35 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:23:36 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_windows-x64_bin.zip
# Fri, 30 Sep 2022 23:23:37 GMT
ENV JAVA_SHA256=aef462584419d1a928f1225061ce4e999d225d636a1406a805962af82e5ca877
# Fri, 30 Sep 2022 23:24:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 Sep 2022 23:24:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c6298a3366175cd1297fbed9781ab93da075956d0549ae06cc0ad3a9f0759b9`  
		Last Modified: Wed, 14 Sep 2022 17:21:32 GMT  
		Size: 593.4 KB (593387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69130dc68926a7dd74a45c56d76c52a89dea16ac92d70aab946e32f9bddfce3d`  
		Last Modified: Wed, 14 Sep 2022 17:21:32 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fc7fa67a5ff75b4568b1c4ae7e98ea07d91433bfd85d115fab3f9d9fd1c762`  
		Last Modified: Wed, 14 Sep 2022 17:21:32 GMT  
		Size: 525.0 KB (524965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067c9b30423cf3eff116bcb14c82bf9aba7f415eb78337d127ad3b404eb4c9f8`  
		Last Modified: Sat, 01 Oct 2022 01:16:44 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdcddd728e95d6edf8b452d324ddc7abc60297b17123871ef6c98ebc7d7d2602`  
		Last Modified: Sat, 01 Oct 2022 01:16:45 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65cc174cfa9936d5a34e13cbed7ccf47389cadf58e5e117f0ea03a4887c4ac15`  
		Last Modified: Sat, 01 Oct 2022 01:16:44 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de38b7b62801bf31fc4a3883088461922441c0ef938568aae8c950e966624a4`  
		Last Modified: Sat, 01 Oct 2022 01:17:04 GMT  
		Size: 192.4 MB (192432787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7741199c6e12af8e4d50ef6d9312a222d7b369817a71783f000407086fa7f47`  
		Last Modified: Sat, 01 Oct 2022 01:16:45 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:20-ea-jdk` - windows version 10.0.17763.3406; amd64

```console
$ docker pull openjdk@sha256:ed261f36d3edef185ab87bd62d414b4c461de51d11550b7f5c0b4dec890df459
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2896475909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d137bca2d1ea8e6abd921982e424ae2298937571138392d30db292f9bb0252a0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 17:06:13 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 Sep 2022 17:06:14 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 14 Sep 2022 17:07:14 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 30 Sep 2022 23:24:38 GMT
ENV JAVA_VERSION=20-ea+17
# Fri, 30 Sep 2022 23:24:39 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk20/17/GPL/openjdk-20-ea+17_windows-x64_bin.zip
# Fri, 30 Sep 2022 23:24:40 GMT
ENV JAVA_SHA256=aef462584419d1a928f1225061ce4e999d225d636a1406a805962af82e5ca877
# Fri, 30 Sep 2022 23:26:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 30 Sep 2022 23:26:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58648929570c8439cbc01e98ebc75618cbe96e946d332763402b53d89cc5639b`  
		Last Modified: Wed, 14 Sep 2022 17:22:14 GMT  
		Size: 349.5 KB (349457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f69dd72d8573f685284949ad83177bf75e72c3d8275d35aa6b4d21f5a480f2b9`  
		Last Modified: Wed, 14 Sep 2022 17:22:14 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59bfc5f723418de82847d7f0e86272a0dc2ec14263a42be94649cbc3d219420b`  
		Last Modified: Wed, 14 Sep 2022 17:22:14 GMT  
		Size: 311.8 KB (311834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213e60afc052a91311ab2912b3c7a09c5c3e34978dc18590bfb2862258f59c1`  
		Last Modified: Sat, 01 Oct 2022 01:17:25 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82067745a860b99cc16743ba122e57ba7a129c82577d410c0af29122f42d1efb`  
		Last Modified: Sat, 01 Oct 2022 01:17:26 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac9fb406669d974505e46651dbec456a75a50a7ea345abc55712a362c6590b0`  
		Last Modified: Sat, 01 Oct 2022 01:17:25 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b92aa7139fa40e8e61a49cd053c454c70c3aad957172c4ffc81f68898efc5f6`  
		Last Modified: Sat, 01 Oct 2022 01:17:46 GMT  
		Size: 192.2 MB (192241364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9883a40a6c5bca46104e958ad106bc6163f05407304db34262fcfd98353b35c4`  
		Last Modified: Sat, 01 Oct 2022 01:17:25 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
